<template>
	<MyBtn>Apple</MyBtn>
	<p>slot /slot 을 출력할 div 사이에 넣어줘야함</p>
	<MyBtn :color="color"><span style="color: red">banana</span></MyBtn>
	<MyBtn large color="blue">ddd</MyBtn>

	<p>속성 상속</p>

	<MyBtn class="hero" stlye="color: red" title="hello~~">apple</MyBtn>
	<MyBtn @click="log">Banana</MyBtn>
</template>

<script>
import MyBtn from "~/components/MyBtn";

export default {
	components: {
		MyBtn,
	},
	data() {
		return {
			color: "#000",
		};
	},
	methods: {
		log() {
			console.log("click!");
		},
	},
};
</script>

<style></style>
