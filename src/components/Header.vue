<template>
  <section>
    <header class="d-flex justify-content-between">
      <img src="../assets/img/logo.png" alt="Spotify Web">
      <select v-model="textToSearch" @change="$emit('sendSearch',textToSearch)" class="form-select form-select-lg mb-3 w-25" aria-label=".form-select-lg example">
        <option value="all" selected>Tutti i generi</option>
        <option value="pop">Pop</option>
        <option value="rock">Rock</option>
        <option value="metal">Metal</option>
        <option value="jazz">Jazz</option>
      </select>
    </header>
  </section>
</template>

<script>
export default {
  name: 'Header',
  data(){
    return{
      textToSearch:'',
    }
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
  select{
    height: 50px;
  }
}
</style>