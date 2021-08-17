<template>
	<div>
		<header-title>
			<template v-slot:title>MCBE Rank 모바일 앱</template>
			<template v-slot:description>앱을 설치하고 MCBE Rank를 더욱 편하게 이용하세요</template>
		</header-title>

		<b-alert show variant="warning">현재 MCBE Rank 앱은 안드로이드 운영체제만 지원하고 있습니다.</b-alert>

		<br/>
		<h4>플레이 스토어 <small>(Android)</small></h4>
		<h6><a href="https://play.google.com/store/apps/details?id=com.taewon.mcberank">다운받기</a></h6>
		<br/><br/>

		<h4>앱 스토어 <small>(iOS)</small></h4>
		<h6><a href="/app">지원되지 않음</a></h6>
		<br/><br/>

		<br/>
	</div>
</template>

<script>
import HeaderTitle from '@/components/HeaderTitle';

export default {
	name: 'app',
	components: {
		HeaderTitle,
	}
};
</script>
