<template>
	<h1 @click="changeMessage">{{ msg }}</h1>
	<h1>{{ reversedMessage }}</h1>
</template>

<script>
export default {
	data() {
		return {
			msg: "hello!",
		};
	},
	computed: {
		reversedMessage() {
			return this.msg.split("").reverse().join("");
		},
	},
	watch: {
		// 특정한 데이터들의 변경사항을 감시하는 옵션
		msg(newValue) {
			console.log("msg:", newValue);
		},
	},
	methods: {
		changeMessage() {
			this.msg = "good!";
		},
	},
};
</script>

/
<style></style>
