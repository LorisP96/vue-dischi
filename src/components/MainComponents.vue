<template>
  <section>
    <div class="container">
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
  mounted() {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music')
    .then((response) => {
      this.albumArray = response.data.response;
    })
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../assets/scss/style.scss';
  section {
    background-color: $bg-color;
    width: 100%;
    padding-top: 80px;
    .container {
      width: 70%;
      height: 100%;
      margin: 0 auto;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
    }
  }
</style>
