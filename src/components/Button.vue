<template>
	<router-link :to="{ name: PageName }">
		<button class="button">
			{{ textButton }}
		</button>
	</router-link>
</template>

<script>
export default {
	name: "Button",
	props: {
		textButton: String,
		name: String,
		PageName: String,
	},
}
</script>

<style lang="scss" scoped>
.button {
	background-color: $primary;
	color: $white;
	font-size: 12px;
	width: auto;
	border-radius: 27px;
	border: solid 3px #ffffff;
	padding: 10px 20px;
	user-select: none;
	float: left;
	filter: drop-shadow(4px 4px 0 $secondaryPink);
	text-transform: uppercase;
	line-height: 150%;
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
		background-color: $white;
		color: $primary;
		cursor: pointer;
		filter: drop-shadow(4px 4px 0 $secondaryPink);
	}
}
</style>
