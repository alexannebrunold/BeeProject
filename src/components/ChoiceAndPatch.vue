<template>
	<div class="choiceAndPatch">
		<h1>Bleached Denim</h1>
		<div class="choiceAndPatch__choice">
			<span class="choiceAndPatch__choice--color">
				<button><img src="@/assets/img/RectangleBleu.jpg" alt="" /></button>

				<button><img src="@/assets/img/RectangleNoir.jpg" alt="" /></button>
			</span>
			<span class="choiceAndPatch__choice--size">
				<label for="size">Taille:</label>

				<select name="pets" id="size">
					<option value="">Choisi ta taille</option>
					<option value="xs">XS</option>
					<option value="s">S</option>
					<option value="m">M</option>
					<option value="l">L</option>
					<option value="xl">XL</option>
					<option value="xxl">XXL</option>
				</select>
			</span>
		</div>

		<h1>Collections</h1>
	</div>
</template>

<script>
export default {
	name: "Button",
	data() {},
	components: {},
	props: {},
	methods: {},
	mounted() {},
}
</script>

<style lang="scss" scoped>
.choiceAndPatch {
	display: flex;
	flex-direction: column;
	&__choice {
		display: flex;
		flex-direction: column;
		align-items: center;
		&--color {
			display: flex;
			flex-direction: row;
		}
		&--size {
			display: flex;
			flex-direction: row;
		}
	}
}
</style>
