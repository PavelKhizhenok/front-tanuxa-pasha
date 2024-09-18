<script lang="ts">
import {defineComponent} from "vue";
import ElementContainer from "@/components/ElementContainer.vue";
import CounterField from "@/components/CounterField.vue";
import CalculateButtonsBlock from "@/components/CalculateButtonsBlock.vue";

export default {
	name: 'App',
	components: {CalculateButtonsBlock, CounterField, ElementContainer},
	data() {
		return {
			count: 0,
		}
	},
	methods: {
		plusCount() {
			this.count++;
		},
		minusCount() {
			this.count--;
		}
	}
}
</script>

<template>
	<div class="app">
		<ElementContainer class="app-cont-field">
			<CounterField
				v-model="count"
			/>
		</ElementContainer>
		<CalculateButtonsBlock
			@plusCount="plusCount"
			@minusCount="minusCount"
		/>
	</div>
</template>

<style scoped>
.app {
	width: 100%;
}

.app-cont-field {
	margin-bottom: 65px;
}
</style>
