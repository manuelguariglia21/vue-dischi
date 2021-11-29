<template>
  <div id="app">
    <Main />
  </div>
</template>

<script>
import Main from './components/Main.vue'
export default {
  name: 'App',
  components: {
    Main
  }
}
</script>

<style lang="scss">
@import './assets/style/vars.scss';
@import './assets/style/generals.scss';
#app{
  height: 100vh;
  overflow: auto;
  background-color: darken($primary-color, 3%);
}
</style>