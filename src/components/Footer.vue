<template>
	<footer class="footer">
		<span class="footer__nav">
			<p>Concept</p>
			<p>À Propos</p>
			<p>Nous trouver</p>
		</span>
		<span class="footer__social">
			<img src="@/assets/img/logos/instagram.svg" alt="" />
			<img src="@/assets/img/logos/facebook.svg" alt="" />
			<img src="@/assets/img/logos/twitter.svg" alt="" />
		</span>
		<span class="footer__copyright">
			<p>© Copyright 2020 Bee Tous droits réservés</p>
		</span>
	</footer>
</template>

<script>
export default {
	name: "Header",
	props: {},
}
</script>

<style lang="scss" scoped>
.footer {
	background-color: $silver;
	width: 100%;
	display: flex;
	flex-direction: row;
	justify-content: space-around;
	font-size: 12px;
	@include laptop {
		font-size: 14px;
		height: 46px;
		align-items: center;
	}
	&__nav {
		display: flex;
		flex-direction: column;
		width: 33.33%;
		@include laptop {
			flex-direction: row;
			justify-content: space-around;
		}
	}
	&__social {
		display: flex;
		flex-direction: row;
		justify-content: space-around;
		width: 33.33%;
		@include laptop {
			justify-content: center;
			align-items: center;
			& img {
				width: 20px;
			}
			& img:nth-child(1) {
				margin-right: 2%;
			}
			& img:nth-child(2) {
				margin-right: 2%;
			}
		}
	}
	&__copyright {
		display: flex;
		flex-direction: row;
		justify-content: space-around;
		width: 33.33%;
	}
}
</style>
