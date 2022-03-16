<template>
	<h1>{{ reversedMessage() }}</h1>
</template>

<script>
export default {
	data() {
		return {
			msg: "hello computed!",
		};
	},
	computed: {
		// 캐싱
		reversedMessage() {
			return this.msg.split("").reverse().join("");
		},
	},
};
</script>

<style></style>
