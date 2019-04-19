<template>
	<v-app class="secondary ma-0 pa-0">
		<v-container fill-height>
			<v-layout align-center justify-center row>
				<v-flex>
					<v-card height="95vh">
						<TheNavbar/>
						<Nuxt id="nuxt-content"/>
					</v-card>
				</v-flex>
			</v-layout>
		</v-container>
	</v-app>
</template>

<script>
	import TheNavbar from "@/components/TheNavbar";

	export default {
		components: {
			TheNavbar
		}
	};
</script>

<style>
</style>
