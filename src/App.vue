<script setup>
import SiteLink from '@/components/SiteLink.vue'
</script>

<template>
	<div class="container">
		<h1>Zach's Home Site</h1>
		<h3>Created with Vue + Vite</h3>

		<div class="spacer">
			<h2>Recent projects:</h2>
		</div>

		<SiteLink
			title="Gym Tool"
			href="https://zachs-gym-tool.netlify.app"
			github="GymTool"
			uses="Nuxt3 and Ionic"
		>
			Tool for creating gym schedules
		</SiteLink>

		<SiteLink
			title="Vue Formulas"
			href=""
			uses="Nuxt3 and Ionic"
			github="VueFormulas"
		>
			Formula calculator components for vue. Sample page created for my
			gen chem class
		</SiteLink>
	</div>
</template>

<style scoped>
/* container is 30rem wide and centered in screen */
.container {
	width: 30rem;
	margin: 0 auto;
}

.spacer {
	margin-top: 4rem;
}

body {
	margin: 0;
	display: flex;
	flex-direction: column;
	align-items: center;
	min-width: 320px;
	min-height: 100vh;
}
</style>
