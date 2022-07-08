<template>
  <section>
    <div class="container">
      <div v-if="albumArray.length < 10" class="loader">Loading...</div>
      <CardComponents v-for="album, index in albumArray" :key="index" :SingleCard="album" />
    </div>
  </section>
</template>

<script>
import CardComponents from '../components/CardComponents.vue';
import axios from 'axios';

export default {
  name: "MainComponents",
  components: { CardComponents },
  data() {
    return {
      albumArray: [],
    }
  },
  methods: {
    getApi() {
      axios.get('https://flynn.boolean.careers/exercises/api/array/music')
    .then((response) => {
      this.albumArray = response.data.response;
    })
    }
  },
  mounted() {
    setTimeout(this.getApi, 3000)
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../assets/scss/style.scss';
  section {
    background-color: $bg-color;
    width: 100%;
    min-height: calc(100vh - 70px);
    padding-top: 80px;
    .container {
      width: 70%;
      height: 100%;
      margin: 0 auto;
      display: flex;
      flex-wrap: wrap;
      justify-content: baseline;
      .loader {
        width: 40%;
        margin: 0 auto;
        height: 300px;
        color: white;
        background-color: $main-color;
        font-weight: 700;
        font-size: 45px;
      }
    }
  }
</style>
