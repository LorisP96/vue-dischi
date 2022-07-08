<template>
  <section>
    <div class="container">
      <!-- <div class="card">
        <div class="card-mini album-image">IMMAGINE</div>
        <div class="card-mini album-info">
          <h2>EZPZDFAS DFSDS ADS asd</h2>
          <div class="artist">NOISY</div>
          <div class="year">1996</div>
        </div>
      </div> -->
    </div>
  </section>
</template>

<script>
export default {
  name: 'MainComponents',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../assets/scss/style.scss';
  section {
    background-color: $bg-color;
    width: 100%;
    height: calc(100vh - 70px);
    padding-top: 80px;
    .container {
      width: 70%;
      height: 100%;
      margin: 0 auto;
      background-color: pink;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      // .card {
      //   width: calc((100% / 5) - 10px);
      //   .card-mini {
      //     background-color: coral;
      //     width: 100%;
      //     aspect-ratio: 1/1;
      //   }
      //   .album-image {
      //     display: flex;
      //     align-items: center;
      //     justify-content: center;
      //     padding: 20px;
      //   }
      //   .album-info {
      //     color: grey;
      //     text-align: center;
      //     h2 {
      //       padding: 10px 0 20px;
      //       color: white;
      //     }
      //     .artist {
      //       font-size: 17px;
      //     }
      //     .year {
      //       font-size: 14px;
      //     }
      //   }
      // }
    }
  }
</style>
