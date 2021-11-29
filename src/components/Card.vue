<template>
  <div class="mg-card">
    <img :src="card.image" :alt="card.title">
    <p class="title">{{card.title}}</p>
    <p class="author">{{card.author}}</p>
    <p class="year">{{card.year}}</p>
  </div>
</template>

<script>
export default {
name: 'Card',
props:{
    card: Object
  }
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
    cursor: pointer;
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