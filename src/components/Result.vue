<template>
		<h1>{{ title }}</h1>
		<Button show='show Text' />
</template>

<script>
	import Button from './Button'
	export default {
		name: 'Header',
		components: {
			Button
		},
		props: {
		title: String
	}
}
</script>