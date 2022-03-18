<template>
	<h1 :class="{ active: isActive }" @click="activate">
		Hello?!({{ isActive }})
	</h1>
</template>

<script>
export default {
	date() {
		return {
			isActive: false,
		};
	},
	methods: {
		activate() {
			this.isActive = true;
		},
	},
};
</script>

<style scoped>
.active {
	color: red;
	font-weight: bold;
}
</style>
