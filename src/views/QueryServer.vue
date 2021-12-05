<template>
	<div>
		<header-title>
			<template v-slot:title>서버 확인</template>
			<template v-slot:description>서버의 정보를 확인할 수 있습니다</template>
		</header-title>

		<b-alert show variant="warning">현재 PMMP 4.0을 사용하는 서버는 조회할 수 없습니다. 빠른 시일 내에 해결하겠습니다.</b-alert>

		<server-form :form="form" :requesting="requesting" :error="error" @submit="onSubmit" />

		<template v-if="Object.keys(server).length">
			<b-card class="mt-3" :header="server.online ? '서버가 온라인입니다.' : '서버가 오프라인인 것 같습니다.'" :title="server.title">
				<server-descriptions :server="server" />
				<player-list :server="server" />
			</b-card>

			<b-button variant="primary" class="mt-3" v-b-toggle.collapse-1>응답 본문</b-button>
			<b-collapse id="collapse-1" class="mt-2">
				<b-card class="mt-3">
					<pre class="m-0">{{ server }}</pre>
				</b-card>
			</b-collapse>
		</template>
	</div>
</template>

<script>
import axios from 'axios';
import HeaderTitle from '@/components/HeaderTitle';
import ServerForm from '@/components/ServerForm';
import ServerDescriptions from '@/components/ServerDescriptions';
import PlayerList from '@/components/PlayerList';

export default {
	name: 'query-server',
	components: {
		HeaderTitle,
		ServerForm,
		ServerDescriptions,
		PlayerList,
	},
	data() {
		return {
			form: { host: '', port: 19132 },
			requesting: false,
			error: {},
			server: {},
		};
	},
	methods: {
		async onSubmit() {
			this.requesting = true;
			this.error = {};

			try {
				const { data } = await axios.get('/api/query', { params: this.form });
				this.server = data;
			} catch (error) {
				this.error = error.response.data;
			} finally {
				this.requesting = false;
			}
		},
	},
};
</script>
