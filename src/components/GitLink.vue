<script setup>
import { ref } from 'vue'

const props = defineProps({
	href: {
		type: String
	}
})

const href = ref(props.href)
if (href.value && !href.value.includes('github.com')) {
	href.value = 'https://github.com/Zach-Mac/' + href.value
}

console.log('href', href.value)
</script>

<template>
	<a v-if="href" :href="href">GitHub</a>
</template>
