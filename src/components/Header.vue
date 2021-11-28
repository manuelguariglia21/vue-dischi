<template>
  <section>
    <header>
      <img src="../assets/img/logo.png" alt="Spotify Web">
    </header>
  </section>
</template>

<script>
export default {
  name: 'Header',
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars.scss';
@import '../assets/style/generals.scss';
header{
  height: 90px;
  line-height: 90px;
  background-color: $primary-color;
  img{
    width: 50px;
    margin-left: 2rem;
  }
}
</style>