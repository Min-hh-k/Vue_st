<template>

  <section>
    <h1>reverse Fruits</h1>
    <ul>
      <li v-for="fruit in reverseFruits" :key="fruit">{{ fruit }}</li>
    </ul>
  </section>

</template>

<script>
export default {
  data() {
    return {
      fruits: [
        'apple','banana', 'cherry'
      ]
    }
  },
  computed: { // 계산된 데이터
    hasFruit() {
      return this.fruits.length > 0
    }
  },
  reverseFruits() {
    return this.fruits.map(fruit => {
      return fruit.split('').reverse().join('')
    } )
  }
}
</script>
