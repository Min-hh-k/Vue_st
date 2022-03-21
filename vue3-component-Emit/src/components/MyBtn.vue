<template>
	<div class="btn">
		<slot name="icon"></slot>
		<slot name="text"></slot>
	</div>
	<h1 @dblclick="$emit('hero', $event)">abc</h1>
	<Input type="text" v-model="msg"></Input>
</template>

<script>
export default {
	emits: ["hero", "changeMsg"],
	data() {
		return {
			msg: "",
		};
	},
	watch: {
		msg() {
			this.$emit("changeMsg", this.msg);
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
