<template>
  <button @click="add">ADD</button>
	<h1>{{ reversedMessage }}</h1>
	<h1>{{ reversedMessage }}</h1>
	<h1>{{ reversedMessage }}</h1>
	<h1>{{ reversedMessage }}</h1>
	<h1>{{ reversedMessage }}</h1>
	<h1>{{ reversedMessage }}</h1>
</template>

<script>
export default {
	data() {
		return {
      //getter, setter
			msg: "hello computed!",
		};
	},
	computed: { //캐싱: 반복될 때 한번만 계산하여 나머지 다표기, 읽기전용
  //Getter : 값을 얻어내는용도
	// 	reversedMessage() {
	// 		return this.msg.split('').reverse().join('')
	// 	}
	

  //getter, setter
  reversedMessage: {
      get() {
        return this.msg.split('').reverse().join('')
      },
      set(value) {
        this.msg = value
      },
    },
  },
  methods: {
    add() {
      this.reversedMessage += '!?'
      // this.msg += '?!'
    }
  }
};
</script>

<style></style>