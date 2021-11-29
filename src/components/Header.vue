<template>
  <section>
    <header class="d-flex justify-content-between">
      <img src="../assets/img/logo.png" alt="Spotify Web">
      <SearchBar @sendSearch="performSearch"/>
    </header>
  </section>
</template>

<script>
import SearchBar from './SearchBar.vue'
export default {
  name: 'Header',
  components:{
    SearchBar,
  },
  data(){
    return{
      textToSearch:''
    }
  },
  methods:{
    performSearch(text){
      this.textToSearch = text;
      console.log(this.textToSearch);
    },
  },
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';
header{
  height: 90px;
  line-height: 90px;
  padding: 20px;
  background-color: $primary-color;
  img{
    width: 50px;
    height: 50px;
  }
}
</style>