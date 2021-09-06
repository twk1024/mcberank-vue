<template>
	<div>
		<header-title>
			<template v-slot:title>MCBE Rank 운영정책</template>
			<template v-slot:description>서버 등록에 대한 안내사항입니다</template>
		</header-title>

		<b-alert show variant="warning">MCBE Rank에 서버를 등록하기 전 아래 내용을 숙지해 주세요.</b-alert>

		<br/>
		<h4>다음과 같은 서버는 등록할 수 있습니다</h4>
		<br/>

		<h6><img src="https://cloud.diamc.kr/images/green-check-icon.jpg" width="15" height="15" alt="check"> 국내를 대상으로 서비스하는 서버</h6>
		<br/>
		<h6><img src="https://cloud.diamc.kr/images/green-check-icon.jpg" width="15" height="15" alt="check"> 정상적으로 작동되고 있는 서버</h6>
		<br/>
		<h6><img src="https://cloud.diamc.kr/images/green-check-icon.jpg" width="15" height="15" alt="check"> 쿼리가 허용된 서버</h6>
		<br/><br/>

		<img src="https://cloud.diamc.kr/images/black_bar.png" alt="BlackBar">
		<br/><br/><br/>
		<h4>다음과 같은 서버는 등록할 수 없습니다</h4>
		<br/>

		<h6><img src="https://cloud.diamc.kr/images/red-x-icon.png" width="13" height="13" alt="no"> 해외 서버</h6>
		<br/>
		<h6><img src="https://cloud.diamc.kr/images/red-x-icon.png" width="13" height="13" alt="no"> 쿼리가 비허용되어 통계 수집이 불가능한 서버</h6>
		<br/><br/>

		<img src="https://cloud.diamc.kr/images/black_bar.png" alt="BlackBar">
		<br/><br/><br/>
		<h4>다음과 같은 서버는 등록 시 삭제될 수 있습니다</h4>
		<br/>
		<h6><img src="https://cloud.diamc.kr/images/red-x-icon.png" width="13" height="13" alt="no"> 개인적인 목적의 서버 (예: 개발용 테스트 서버)</h6>
		<br/>
		<h6><img src="https://cloud.diamc.kr/images/red-x-icon.png" width="13" height="13" alt="no"> 특정 플레이어를 대상으로 하는 비공개 서버 (예: 친구와 플레이하기 위한 야생서버)</h6>
		<br/>
		<h6><img src="https://cloud.diamc.kr/images/red-x-icon.png" width="13" height="13" alt="no"> 접속자 수와 같은 순위에 영향을 주는 정보를 임의로 조작한 서버</h6>
		<br/><br/>
	</div>
</template>

<script>
import HeaderTitle from '@/components/HeaderTitle';

export default {
	name: 'terms',
	components: {
		HeaderTitle,
	}
};
</script>
