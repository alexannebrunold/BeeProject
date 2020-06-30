<template>
	<div class="personnalisation page">
		<ViewJacket />
		<ChoiceAndPatch />
		<!-- <Footer /> -->
	</div>
</template>

<script>
import ViewJacket from "@/components/ViewJacket.vue"
import ChoiceAndPatch from "@/components/ChoiceAndPatch.vue"
// import Footer from "@/components/Footer.vue"
export default {
	name: "Home",
	components: {
		ViewJacket,
		ChoiceAndPatch,
		// Footer,
	},
}
</script>

<style lang="scss" scoped>
.personnalisation {
	width: 100%;
	display: flex;
	flex-direction: column;
}
</style>
