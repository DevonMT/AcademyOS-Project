<template>
	<v-container id="links-layout">
		<v-layout row wrap>
			<v-flex :key="index" v-for="(link, index) in links" xs3>
				<v-list>
					<v-list-group no-action subheader>
						<template v-slot:activator>
							<v-list-tile>
								<v-list-tile-content>
									<v-list-tile-title>{{ link.name }}</v-list-tile-title>
								</v-list-tile-content>
							</v-list-tile>
						</template>
						<v-list-tile
							:href="page.url"
							:key="index"
							color="primary"
							target="_blank"
							v-for="(page, index) in link.pages"
						>{{page.name}}</v-list-tile>
					</v-list-group>
				</v-list>
			</v-flex>
		</v-layout>
	</v-container>
</template>

<script>
	export default {
		name: "Links",
		data() {
			return {
				links: [
					{
						name: "first link",
						pages: [
							{
								name: "first page",
								url: "http://www.google.com"
							}
						]
					}
				]
			};
		}
	};
</script>

<style scoped>
	#links-layout {
		overflow-y: scroll;
	}
</style>
