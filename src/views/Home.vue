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

		<section class="home__choice">
			<h1 class="home__choice--title">Choisis ton modèle</h1>
			<div class="home__choice__choices">
				<div class="home__choice__choices__firstChoice">
					<img src="@/assets/img/Veste_Jean_Bleached.jpg" alt="" />
					<span class="home__choice__choices__firstChoice--buttonChoice">
						<Button textButton="Personnaliser" PageName="#" />
					</span>

					<p>À partir de 60€</p>
				</div>
				<div class="home__choice__choices__secondChoice">
					<img src="@/assets/img/Veste_Jean_Noire.jpg" alt="" />
					<span class="home__choice__choices__secondChoice--buttonChoice">
						<Button textButton="Personnaliser" PageName="#" />
					</span>
					<p>À partir de 60€</p>
				</div>
			</div>
		</section>
		<section class="home__fans">
			<h1>Ils sont déjà fans de Bee</h1>
			<span class="home__fans--button">
				<Button textButton="Suivez-nous sur Instagram" PageName="#" />
			</span>
			<div class="home__fans__images">
				<img src="@/assets/img/Star_1.jpg" alt="" class="div1" />
				<img src="@/assets/img/Star_2.jpg" alt="" class="div2" />
				<img src="@/assets/img/Star_3.jpg" alt="" class="div3" />
				<img src="@/assets/img/Star_4.jpg" alt="" class="div4" />
			</div>
		</section>

		<section class="home__values">
			<h1>Nos valeurs</h1>
			<div class="home__values__all">
				<div>
					<img src="@/assets/img/logos/unicorn.svg" alt="" />
					<p>Vegan</p>
				</div>
				<div>
					<img src="@/assets/img/logos/chanvre.svg" alt="" />
					<p>CHanvre</p>
				</div>
				<div>
					<img src="@/assets/img/logos/local.svg" alt="" />
					<p>Local</p>
				</div>
				<div>
					<img src="@/assets/img/logos/green.svg" alt="" />
					<p>Less impact</p>
				</div>
			</div>
		</section>
		<Footer />
	</div>
</template>

<script>
import Button from "@/components/Button.vue"
import Footer from "@/components/Footer.vue"
export default {
	name: "Home",
	components: {
		Button,
		Footer,
	},
}
</script>

<style lang="scss">
.home {
	&__header {
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
	&__contexte {
		margin-top: 20%;
		height: 50vh;
		@include tablet {
			margin-top: 4%;
			padding-bottom: 6%;
			height: auto;
		}
		@include laptop {
			margin-top: -30%;
			float: right;
			width: 40%;
		}
		& h2 {
			color: $secondaryOrange;
			font-family: "Baloo Bhai 2";
			font-weight: 600;
			font-size: 24px;
			@include tablet {
				font-size: 32px;
				margin-bottom: 2%;
			}
			@include laptop {
				color: $white;
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
			@include tablet {
				font-size: 20px;
			}
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
			display: none;
			font-family: "Montserrat";
			text-transform: uppercase;
			@include tablet {
				padding: 10px 40px;
				font-size: 16px;
			}
			@include laptop {
				font-size: 16px;
				display: block;
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
	&__choice {
		width: 100%;
		& p {
			@include tablet {
				font-size: 20px;
			}
		}
		&__choices {
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;
			width: 100%;
			@include laptop {
				flex-direction: row;
				justify-content: space-around;
			}
			&__firstChoice {
				display: flex;
				flex-direction: column;
				justify-content: center;
				align-items: center;
				margin-bottom: 8%;
				@include laptop {
					margin-bottom: 0%;
				}
				& img {
					width: 80%;
				}
				&--buttonChoice {
					margin-bottom: 4%;
				}
			}
			&__secondChoice {
				display: flex;
				flex-direction: column;
				justify-content: center;
				align-items: center;
				& img {
					width: 80%;
				}
				&--buttonChoice {
					margin-bottom: 4%;
				}
			}
		}
	}
	&__fans {
		display: flex;
		flex-direction: column;
		align-items: center;
		padding-top: 8%;
		margin-bottom: 6%;
		&--button {
			margin-top: -4%;
			margin-bottom: 2%;
		}
		&__images {
			& img:nth-child(2) {
				display: none;
			}
			& img:nth-child(3) {
				display: none;
			}
			@include laptop {
				display: grid;
				grid-template-columns: 1fr 0.5fr 1fr;
				grid-row: 1fr 1fr;
				gap: 1px 1px;
				grid-template-areas: ". . ." ". . .";
				justify-items: center;
				align-content: center;
				& img:nth-child(1) {
					grid-area: 1 / 1 / 2 / 2;
				}
				& img:nth-child(2) {
					grid-area: 1 / 2 / 2 / 3;
					margin-top: 8%;
					display: block;
				}
				& img:nth-child(3) {
					grid-area: 1 / 2 / 2 / 3;
					margin-top: 90%;
					display: block;
				}
				& img:nth-child(4) {
					grid-area: 1 / 3 / 2 / 4;
				}
			}
			& img {
				width: 80%;
				margin: 4% 0;
			}
		}
	}
	&__values {
		padding-bottom: 6%;
		&__all {
			display: flex;
			flex-direction: column;
			@include laptop {
				flex-direction: row;
				justify-content: space-around;
				height: 80%;
			}
		}
	}
}
</style>
