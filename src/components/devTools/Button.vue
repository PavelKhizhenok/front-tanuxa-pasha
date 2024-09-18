<script lang="ts">
	export default {
		name: 'Button',
		props: {

		},
		methods: {
			clickButton() {
				this.$emit('clickButton');
			}
		}
	}
</script>

<template>
	<div class="button-container">
		<button
				class="button"
				@click="clickButton"
		>
			<slot></slot>
		</button>
	</div>
</template>

<style scoped>
.button {
	width: 100%;
	height: 100%;
	border: none;
	background: none;
}

.button-container {
	width: 100%;
	height: 100%;
	display: flex;
}
</style>