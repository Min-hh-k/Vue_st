<template>
	<MyBtn @hero="log" @change-msg="logMsg">
		<template v-slot:icon><span>(B)</span></template>
		<template #text><span>Banana</span></template>
	</MyBtn>
	// @click 대신 다른 거 넣어도 됨. emits:['hero'],
	<h2 ref="hello">hello! world</h2>
	// ref
</template>

<script>
import MyBtn from "~/components/MyBtn";

export default {
	components: {
		MyBtn,
	},
	data() {
		return {};
	},
	methods: {
		log(event) {
			console.log("click!");
			console.log(event);
		},
		logMsg(msg) {
			console.log(msg);
		},
	},
	mounted() {
		console.log(this.$refs.hello);
	},
};
</script>

<style></style>
