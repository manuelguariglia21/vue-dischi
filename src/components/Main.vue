<template>

<section>
  <Header @sendSearch="performSearch"/>
  <main>
    <Card 
    v-for="(card, index) in filteredCards"
        :key="index"
        :card="card"
    />
  </main>
</section>
  
</template>

<script>
import axios from 'axios';
import Card from './Card.vue'
import Header from './Header.vue'
export default {
  name: 'Main',
  components:{
    Header,
    Card,
  },
  data(){
    return{
      cards: [],
      loaded:false,
      apiUrl: 'https://flynn.boolean.careers/exercises/api/array/music',
      textToSearch:''
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
    },

    performSearch(text){
      this.textToSearch = text;
      console.log(this.textToSearch);
    },
  },
  mounted(){
    this.getApi();
  },
  computed:{
    filteredCards(){
      if(this.textToSearch === '' || this.textToSearch === 'all'){
        return this.cards;
      }
      const arrayFiltered = this.cards.filter( item => {
        return item.genre.toUpperCase().includes(this.textToSearch.toUpperCase());
      });
      return arrayFiltered;
    }
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