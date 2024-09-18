<script lang="ts">
export default {
	name: 'CounterField',
	props: {
		modelValue : {
			type: Number,
			required: true,
		}
	}
}
</script>

<template>
	<div class="counter-field">
		{{ modelValue }}
	</div>
</template>

<style scoped>
.counter-field {
	padding: 20px 0;
	font-size: 30px;
}
</style>