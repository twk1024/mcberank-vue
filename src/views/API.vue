<template>
	<div>
		<header-title>
			<template v-slot:title>MCBE Rank API</template>
			<template v-slot:description>API 사용에 대한 안내사항입니다</template>
		</header-title>

		<br/>
		<h3>API Documentation</h3>
		<img src="https://cloud.diamc.kr/images/black_bar.png" alt="BlackBar">
		<br/><br/>
		<h4>서버 정보 불러오기</h4>
		<br/>

		<h6>특정 서버의 정보만 불러오는 경우</h6>
        <p>GET <a href="http://be.diamc.kr/api/servers/diamc.kr:19131">http://be.diamc.kr/api/servers/[hostname]:[port]</a></p>
		<br/>
		<h6>모든 서버의 정보를 불러오는 경우</h6>
		<p>GET <a href="http://be.diamc.kr/api/servers">http://be.diamc.kr/api/servers</a></p>

		<br/>
		<img src="https://cloud.diamc.kr/images/black_bar.png" alt="BlackBar">
		<br/><br/>
		<h4>서버 쿼리 조회하기</h4>
		<br/>
        <p>GET <a href="http://be.diamc.kr/api/query?host=diamc.kr&port=19132">http://be.diamc.kr/api/query?host=[hostname]&port=[port]</a></p>
        
		<br/>
		<img src="https://cloud.diamc.kr/images/black_bar.png" alt="BlackBar">
		<br/><br/>
		<h4>특정 기간의 서버 접속자 기록 불러오기</h4>
		<br/>
		<p>GET <a href="https://be.diamc.kr/api/stats/diamc.kr:19131/numplayers?from=2021-08-17T23:58:50.319Z&to=2021-08-18T01:00:27.775Z">https://be.diamc.kr/api/stats/[hostname]:[port]/numplayers?from=YY-MM-DD:Hour:Minute:Seconds&to=YY-MM-DD:Hour:Minute:Seconds</a></p>
		<br/>
		<h6>- [YY-MM-DD:Hour:Minute:Seconds]는 [년도-월-일:시간:분:초]를 의미하며 2021-10-24:06:30:21와 같은 UTC 형식으로 입력해야 합니다</h6>
		<h6>- 년도를 제외한 나머지 항목은 생략할 수 있습니다</h6>

		<br/>
		<img src="https://cloud.diamc.kr/images/black_bar.png" alt="BlackBar">
		<br/><br/>
		<h4>플러그인 정보 불러오기</h4>
		<br/>
		<p>GET <a href="http://be.diamc.kr/api/plugins">http://be.diamc.kr/api/plugins</a></p>
		<br/><br/>
		
		<br/>
		<h3>API 사용예제</h3>
		<img src="https://cloud.diamc.kr/images/black_bar.png" alt="BlackBar">
		<br/><br/>
		<h5>McbeRank-Website-API</h5>
		<p>php를 사용하여 웹사이트에서 MCBE Rank API를 사용합니다.</p>
		<p><a href="https://github.com/twk1024/McbeRank-Website-API">Source Code</a></p>
		<br/>
		
		<h5>BedrockRank</h5>
		<p>PMMP에서 서버 순위를 조회 및 출력합니다.</p>
        <p><a href="https://github.com/twk1024/BedrockRank">Source Code</a></p>
		<br/>
	</div>
</template>

<script>
import HeaderTitle from '@/components/HeaderTitle';

export default {
	name: 'api',
	components: {
		HeaderTitle,
	}
};
</script>
