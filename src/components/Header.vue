<template>
	<header class="header">
		<nav></nav>
		<h1 class="home__header--title">BEE</h1>
	</header>
</template>

<script>
export default {
	name: "Header",
	props: {},
}
</script>

<style lang="scss" scoped>
.header {
	background-color: $primary;
	height: 80vh;
	width: 100%;
	background-image: url("~@/assets/img/jacket1.svg");
	background-size: cover;
	background-position: center;
	@include laptop {
		background: url("~@/assets/img/bgHomeDesktop.jpg");
		background-repeat: no-repeat;
	}
	&--title {
		font-family: "Baloo Bhai 2";
		font-weight: 500;
		font-size: 48px;
		color: $white;
	}
}
</style>
