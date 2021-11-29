<template>
  <main>
    <Card 
    v-for="(card, index) in cards"
        :key="index"
        :card="card"
    />
  </main>
</template>

<script>
import axios from 'axios';
import Card from './Card.vue'
export default {
  name: 'Main',
  components:{
    Card,
  },
  data(){
    return{
      cards: [],
      loaded:false,
      apiUrl: 'https://flynn.boolean.careers/exercises/api/array/music'
    }
  },
  methods:{
    getApi(){
      axios.get(this.apiUrl)
        .then( r => {
          this.cards = r.data.response;
          this.loaded = true;
        })
        .catch( e => {
          console.log(e);
        })
    }
  },
  mounted(){
    this.getApi();
  }
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