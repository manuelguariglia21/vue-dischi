<template>
  <main>
    <Card />
  </main>
</template>

<script>
import Card from './Card.vue'
export default {
  name: 'Main',
  components:{
    Card,
  },
}
</script>

<style lang="scss" scoped>
main{
  width: 80%;
  margin: 50px auto;
  display: flex;
  justify-content: start;
  flex-wrap: wrap;
  overflow: auto;
}
</style>