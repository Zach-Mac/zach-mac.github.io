<script setup>
import { ref } from 'vue'

const props = defineProps({
	title: {
		type: String,
		default: ''
	},
	href: {
		type: String,
		default: ''
	},
	github: {
		type: String,
		default: ''
	},
	uses: {
		type: String,
		default: ''
	}
})

const github = ref(props.github)
if (github.value && !github.value.includes('github.com')) {
	github.value = 'https://github.com/Zach-Mac/' + github.value
}

const link = ref(null)

function onCardClick() {
	if (link.value) {
		console.log(link.value)
		link.value.click()
	}
}
</script>

<template>
	<div :class="['card', href ? 'cardHover' : '']" @click="onCardClick()">
		<h2 class="title">
			<a v-if="href" :href="href" ref="link" class="titleLink">{{
				title
			}}</a>
			<a v-else class="notLink titleLink">{{ title }}</a>
		</h2>
		<p class="uses">Made with {{ uses }}</p>
		<p><slot></slot></p>
		<a v-if="github" :href="github">Github</a>
	</div>
</template>

<style scoped>
.titleLink {
	text-decoration: none;
}

button {
	margin-left: 1rem;
}

.title {
	margin-bottom: 0.5rem;
}

.uses {
	margin-top: 0;
	margin-bottom: 0;
	font-size: 0.8rem;
}

.row {
	align-self: flex-start;
	display: flex;
	flex-direction: row;
	justify-content: flex-start;
	align-items: center;
}

p {
	padding-left: 1rem;
	padding-right: 1rem;
}

.card {
	text-align: justify;
	display: flex;
	flex-direction: column;
	align-items: center;
	margin: 1rem;
	padding: 1rem;
	border-radius: 0.5rem;
	background-color: #121212;
	box-shadow: 0 0.25rem 0.5rem rgba(0, 0, 0, 0.125);
}

.cardHover:hover {
	cursor: pointer;
	box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.25);
}

.notLink {
	cursor: default;
}
.notLink:hover {
	color: #646cff;
}

h5 {
	margin-top: 0.5rem;
}
</style>
