<template>
	<div>
		<header-title>
			<template v-slot:title>문의하기</template>
			<template v-slot:description>아래의 방법에 따라 문의해 주세요</template>
		</header-title>

		<!-- <b-alert show variant="info">상황에 따라 답변이 늦어질 수 있습니다</b-alert> -->

		<br/>
		<h4>카카오톡 플러스친구 <small>(@도끼다이아)</small></h4>
		<h6><a href="https://pf.kakao.com/_kBhrd">메세지 보내기</a></h6>
		<br/><br/>

		<h4>이메일 <small>(support@diamc.kr)</small></h4>
		<h6><a href="mailto:support@diamc.kr">이메일 보내기</a></h6>
		<br/>
	</div>
</template>

<script>
import HeaderTitle from '@/components/HeaderTitle';

export default {
	name: 'support',
	components: {
		HeaderTitle,
	}
};
</script>
