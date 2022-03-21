<template>
	<div
		:class="{ large: large }"
		:style="{ backgroundColor: color }"
		class="btn"
	>
		<slot></slot>
	</div>
	<h1 :class="$attrs.class" :style="$attrs.style"></h1>
	<h1 v-bind="$attrs"></h1>
</template>

<script>
export default {
	inheritAttrs: false,
	created() {
		console.log(this.$attrs);
	},
	props: {
		color: {
			type: String,
			default: "gray",
		},
		large: {
			type: Boolean,
			default: false,
		},
	},
};
</script>

<style scoped="scss">
.btn {
	display: inline-block;
	margin: 4px;
	padding: 6px 12px;
	border-radius: 4px;
	background-color: gray;
	color: white;
	cursor: pointer;
	&.large {
		font-size: 20px;
		padding: 10px 20px;
	}
}
</style>
