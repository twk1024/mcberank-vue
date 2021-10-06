<template>
	<!-- copyright -->
	<footer class="footer bg-light">
		<div class="container py-4 text-muted">
			<a href="https://github.com/McbeRank" class="text-secondary" style="font-size: 1.2em"> <i class="fa fa-github"></i> Github </a>
			<a class="text-secondary" style="font-size: 1.2em">&nbsp; | &nbsp;&nbsp;</a>
			<a href="/app" class="text-secondary" style="font-size: 1.2em"> <i class="fa fa-mobile"></i> Mobile App </a>

			<div class="my-2">
				<router-link :to="{ name: 'terms' }"><small>운영 정책</small></router-link><small> - Copyright 2021. McbeRank All rights reserved.</small>
			</div>
		</div>
	</footer>
</template>

<script>
export default {
	name: 'Footer',
};
</script>

<style scoped>
a {
	text-decoration: none;
}
</style>
