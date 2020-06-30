<template>
	<div class="viewJacket">
		<header></header>
		<span class="viewJacket__first">
			<div class="viewJacket__first--zoom">
				<img src="@/assets/img/ZoomIn.svg" alt="" />
				<img src="@/assets/img/ZoomOut.svg" alt="" />
			</div>
			<div class="viewJacket__first--img">
				<img src="@/assets/img/Veste_Jean_Bleached.jpg" alt="" ref="imageFace" class="imageFace" />
				<img src="@/assets/img/veste.jpg" alt="" ref="imageBack" class="imageBack" />
			</div>
		</span>
		<span class="viewJacket__second">
			<div class="viewJacket__second--arrows">
				<img src="@/assets/img/undo.svg" alt="" class="leftArrow" v-on:click="turnRight" />
				<!-- <img src="@/assets/img/leftArrow.svg" alt="" class="rigthArrow" v-on:click="turnRight" /> -->
			</div>
			<div class="">
				<img src="@/assets/img/bin.svg" alt="" />
			</div>
		</span>
	</div>
</template>

<script>
export default {
	name: "Button",
	props: {},
	methods: {
		turnRight() {
			if (this.$refs.imageFace.style.display !== "none") {
				this.$refs.imageFace.style.display = "none"
				this.$refs.imageBack.style.display = "block"
			} else {
				this.$refs.imageFace.style.display = "block"
				this.$refs.imageBack.style.display = "none"
			}
		},
	},
	mounted() {
		console.log(this.$refs)
	},
}
</script>

<style lang="scss" scoped>
.viewJacket {
	width: 100%;

	&__first {
		display: flex;
		flex-direction: row;
		align-items: center;
		&--zoom {
			// display: flex;
			// flex-direction: column;
			// height: 100%;
			// justify-content: space-around;
			// width: auto;
			& img:nth-child(1) {
				margin-bottom: 80%;
			}
		}
		&--img {
			width: 90%;
			& img {
				width: 251.41px;
				height: 285.28px;
			}
		}
	}
	&__second {
		display: flex;
		flex-direction: row;
		justify-content: space-around;
		align-items: center;
		width: 60%;
		margin-left: 40%;
		&--arrows {
			display: flex;
			flex-direction: row;
		}
	}
}
header {
	height: 40px;
	background-color: $primary;
}

.imageFace {
	display: block;
}
.imageBack {
	display: none;
}

.leftArrow {
	width: 16%;
}
</style>
