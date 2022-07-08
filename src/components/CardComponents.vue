<template>
  <div class="card">
    <div class="album-image">
      <img :src="SingleCard.poster" :alt="SingleCard.genre">
    </div>
    <div class="album-info">
          <h2>{{ SingleCard.title }}</h2>
          <div class="artist">{{ SingleCard.author }}</div>
          <div class="year">{{ SingleCard.year }}</div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'CardComponents',
  props: { 
    SingleCard: Object,
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../assets/scss/style.scss';
  .card {
        width: calc((100% / 5) - 50px);
        margin-bottom: 20px;
        background-color: $main-color;
        margin: 20px;
        .album-image {
          display: flex;
          align-items: center;
          justify-content: center;
          padding: 20px;
          aspect-ratio: 1/1;
          img {
            width: 100%;
            height: 100%;
            object-fit: cover;
          }
        }
        .album-info {
          color: grey;
          text-align: center;
          padding: 10px;
          h2 {
            padding: 10px 0 20px;
            color: white;
          }
          .artist {
            font-size: 17px;
          }
          .year {
            font-size: 14px;
          }
        }
      }
</style>
