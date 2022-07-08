<template>
  <header>
    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/19/Spotify_logo_without_text.svg/2048px-Spotify_logo_without_text.svg.png" alt="logo">
  </header>
</template>

<script>
export default {
  name: 'HeaderComponents',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../assets/scss/style.scss';
  header {
    height: 70px;
    background-color: $main-color;
    display: flex;
    align-items: center;
    img {
      width: 42px;
      margin-left: 20px;
    }
  }
</style>
