<script lang="ts">

import Button from "@/components/devTools/Button.vue";
import ElementContainer from "@/components/ElementContainer.vue";

export default {
	name: "CalculateButtonsBlock",
	components: {ElementContainer, Button},
	methods: {
		plusCount() {
			this.$emit('plusCount');
		},
		minusCount() {
			this.$emit('minusCount');
		}
	}
}
</script>

<template>
	<div class="calculate-buttons-block_list">
		<ElementContainer
			class="calculate-buttons-block_list_item"
		>
			<Button
				@clickButton="plusCount"
			>
				<div class="calculate-buttons-block_list_item_text">+</div>
			</Button>
		</ElementContainer>
		<ElementContainer
				class="calculate-buttons-block_list_item"
		>
			<Button
					@clickButton="minusCount"
			>
				<div class="calculate-buttons-block_list_item_text">-</div>
			</Button>
		</ElementContainer>
	</div>
</template>

<style scoped>
.calculate-buttons-block_list {
	display: flex;
	justify-content: space-between;
}

.calculate-buttons-block_list_item {
	max-width: 160px;
}

.calculate-buttons-block_list_item_text {
	font-size: 30px;
	padding: 15px 0;
}
</style>