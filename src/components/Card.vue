<template>
  <div class="mg-card">
    <img src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="nome">
    <p class="title">New Jersey</p>
    <p class="author">Bon Jovi</p>
    <p class="year">1988</p>
  </div>
</template>

<script>
export default {
name: 'Card',
}
</script>

<style lang="scss">
  @import '../assets/style/vars.scss';
  @import '../assets/style/generals.scss';
  .mg-card{
    background-color: $primary-color;
    color: white;
    min-height: 300px;
    width: calc(100% / 5 - 20px);
    margin:5px 10px;
    display: flex;
    flex-direction: column;
    align-items: center;
    img{
      width: 80%;
      margin: 10px auto;
    }
    p{
      padding: 0;
      margin: 0;
    }
    .title{
      text-transform: uppercase;
      font-weight: 700;
      margin-bottom: 10px;
    }
    .author, .year{
      color: gray;
    }
  }
</style>