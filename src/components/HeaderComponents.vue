<template>
  <header>
    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/19/Spotify_logo_without_text.svg/2048px-Spotify_logo_without_text.svg.png" alt="logo">
    <select v-model="genreSelected" @change="$emit('changeGenre', genreSelected)" name="genre-selection" id="genre-selection">
        <option value="All">All</option>
        <option value="Rock">Rock</option>
        <option value="Pop">Pop</option>
        <option value="Jazz">Jazz</option>
        <option value="Metal">Metal</option>
      </select>
  </header>
</template>

<script>
export default {
  name: 'HeaderComponents',
  data() {
    return {
      genreSelected: 'all'
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../assets/scss/style.scss';
  header {
    height: 70px;
    background-color: $main-color;
    display: flex;
    justify-content: space-between;
    align-items: center;
    img {
      width: 42px;
      margin-left: 20px;
    }
    select {
      height: 40px;
      width: 140px;
      font-weight: 600;
      font-size: 25px;
      text-align: center;
      background-color: $main-color;
      color: white;
      border-radius: 10px;
      margin-right: 20px;
    }
  }
</style>
