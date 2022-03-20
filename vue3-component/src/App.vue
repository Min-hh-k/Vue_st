<template>
	<MyBtn>Apple</MyBtn>
	<p>slot /slot 을 출력할 div 사이에 넣어줘야함</p>
	<MyBtn :color="color"><span style="color: red">banana</span></MyBtn>
	<MyBtn large color="blue">ddd</MyBtn>
	<MyBtn>sss</MyBtn>
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
};
</script>

<style></style>
