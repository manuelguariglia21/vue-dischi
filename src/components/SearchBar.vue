<template>
  <select v-model="textToSearch" @change="$emit('sendSearch',textToSearch)" class="form-select form-select-lg mb-3 w-25" aria-label=".form-select-lg example">
  <option selected>Tutti i generi</option>
  <option value="pop">Pop</option>
  <option value="rock">Rock</option>
  <option value="metal">Metal</option>
  <option value="jazz">Jazz</option>
</select>
</template>

<script>
export default {
  name: 'SearchBar',
}
</script>

<style lang="scss" scoped>
  select{
    height: 50px;
  }
</style>