<template>
	<div class="home page">
		<header class="home__header">
			<nav></nav>
			<h1 class="home__header--title">BEE</h1>
		</header>
		<section class="home__contexte">
			<h2>Be yourself, patch'it. *</h2>
			<p>
				Revivez les années 70 avec notre collection de plus de 100 stickers pour patcher votre
				jacket.
			</p>
			<button>Créer votre veste</button>
		</section>
	</div>
</template>

<script>
export default {
	name: "Home",
	components: {},
}
</script>

<style lang="scss">
.home {
	background-image: url("~@/assets/img/jacket1.svg");
	width: auto;
	background-size: cover;
	background-position: center;
	@include laptop {
		background: url("~@/assets/img/bgHomeDesktop.jpg");
		background-repeat: no-repeat;
	}
	&__header {
		background-color: $primary;
		height: 55px;
		width: 100%;
		&--title {
			font-family: "Baloo Bhai 2";
			font-weight: 500;
			font-size: 48px;
			color: $white;
			padding-top: 2%;
		}
	}
	&__contexte {
		margin-top: 120%;
		@include laptop {
			margin-top: 10%;
			float: right;
			width: 40%;
		}
		& h2 {
			color: $secondaryOrange;
			font-family: "Baloo Bhai 2";
			font-weight: 400;
			font-size: 24px;
			@include laptop {
				color: $secondaryPink;
				width: 400px;
				text-align: left;
				font-size: 60px;
				margin-bottom: 8%;
			}
		}
		& p {
			color: $black;
			font-family: "Montserrat";
			font-size: 12px;
			@include laptop {
				width: 500px;
				text-align: left;
				font-size: 20px;
				margin-bottom: 8%;
			}
		}
		& button {
			background-color: $white;
			color: $primary;
			font-size: 12px;
			width: auto;
			border-radius: 27px;
			border: solid 3px #ffffff;
			padding: 10px 20px;
			user-select: none;
			float: left;

			filter: drop-shadow(4px 4px 0 $secondaryPink);
			@include tablet {
				padding: 10px 40px;
				font-size: 16px;
			}
			@include laptop {
				font-size: 16px;
			}
			@include pc {
				font-size: 22px;
			}
			&:hover {
				border: solid 3px rgb(255, 255, 255);
				background-color: $primary;
				color: $white;
				cursor: pointer;
				filter: drop-shadow(4px 4px 0 $secondaryPink);
			}
		}
	}
}
</style>
