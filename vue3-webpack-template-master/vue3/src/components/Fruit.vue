<template>
  <li>{{ name }}?!</li>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      default: '',
    }
  }
}
</script>

<style scoped lang="scss"> // scoped 현재 Fruit 내용에만 영향 미침
  h1 {
    color: red !important
  }
</style>