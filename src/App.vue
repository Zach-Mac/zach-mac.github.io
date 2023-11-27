<script setup>
import SiteLink from '@/components/SiteLink.vue'
import GitLink from '@/components/GitLink.vue'
</script>

<template>
	<div class="container">
		<h1>Zach's Home Site</h1>
		<h5>Created with Vue + Vite</h5>

		<a href="https://github.com/Zach-Mac/">https://github.com/Zach-Mac/</a>

		<div class="spacer">
			<h2>Recent projects:</h2>
		</div>

		<SiteLink
			title="Zachs Flags"
			uses="Nuxt3 and Ionic"
			href="https://zachsflags.vercel.app"
			github="FlagCompare"
		>
			View country flags side by side
		</SiteLink>

		<SiteLink
			title="Zachs Tools"
			uses="Nuxt3 and Ionic"
			href="https://zachstools.vercel.app"
			github="ZachsTools"
		>
			Set of tools
			Gym Tool: to create workout schedules
			Calendar Tool: to quickly add/move many events on Google Calendar 
		</SiteLink>

		<SiteLink title="Vue Formulas" 
			  uses="Nuxt3 and Ionic" 
			  href="https://zachs-vue-formulas.netlify.app" 
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
