<template>
	<div>
		<ViewJacket />
		<Footer />
	</div>
</template>

<script>
import ViewJacket from "@/components/ViewJacket.vue"
import Footer from "@/components/Footer.vue"
export default {
	name: "Home",
	components: {
		ViewJacket,
		Footer,
	},
}
</script>
