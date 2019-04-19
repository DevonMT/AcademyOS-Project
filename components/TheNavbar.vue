<template>
	<nav>
		<v-toolbar card color="secondary darken-2" dark>
			<v-toolbar-items>
				<v-btn flat to="/">
					<v-toolbar-title>AcademyOS</v-toolbar-title>
				</v-btn>
			</v-toolbar-items>
			<v-spacer/>
			<v-toolbar-items>
				<v-form class="mr-4 pt-1">
					<v-text-field
						@click:append="submitPass"
						append-icon="play_arrow"
						clearable
						label="AOS Pass"
						type="password"
						v-model="aosPass"
					></v-text-field>
				</v-form>
				<v-btn flat to="/links">Links</v-btn>
				<v-btn flat to="/calc">Calculation</v-btn>
				<v-btn flat to="/chat">Chat</v-btn>
				<v-btn flat to="/procedures">Procedures</v-btn>
			</v-toolbar-items>
		</v-toolbar>
	</nav>
</template>

<script>
	export default {
		name: "Navbar",
		data() {
			return {
				aosPass: null
			};
		},
		methods: {
			submitPass() {
				console.log(this.aosPass);
			}
		}
	};
</script>

<style>
	div.v-toolbar__content {
		padding: 0;
	}
</style>
