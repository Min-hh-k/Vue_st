<template>
  <h1 @click="increase">{{ count }}</h1>
  <div v-if="count > 4">
    4보다 큽니다!
  </div>
  <ul>
    <Fruit v-for="fruit in fruits"
    :key="fruit"
    :name="fruit">
      {{fruit}}
    </Fruit>
  </ul>


</template>

<script>
import Fruit from '~/components/Fruit'
export default {
  components: {
    Fruit // 객체 이름과 데이터 이름이 같으면 Fruit: Fruit 에서: Fruit 생략 가능
  },
  data() {
    return {
      count: 0, //반응성,, 데이터를 갱신하면 화면도 바뀐다
      fruits: ['Apple','Banana','Cherry']
    }
  },
  methods: {
    increase() {
      this.count += 1
    }
  }
}
</script>


<style lang="scss">
  h1 {
    font-size: 50px;
    color: tomato;
  }
  ul {
    li {
      font-size: 40px;
    }
  }
</style>
