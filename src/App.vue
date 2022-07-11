<template>
  <div id="app">
    <HeaderComponents @changeGenre="filteredGenre" />
    <main>
      <MainComponents :filteredArray="filteredArray" :albumArray="albumArray" />
    </main>
  </div>
</template>

<script>
import HeaderComponents from './components/HeaderComponents.vue';
import MainComponents from './components/MainComponents.vue';
import axios from 'axios';


export default {
  name: 'App',
  data() {
    return {
      // activeGenre: '',
      albumArray: [],
      filteredArray: [],
    }
  },
  components: {
    HeaderComponents,
    MainComponents
  },
  methods: {
    filteredGenre(value) {
      if(value !== 'All') {
        this.filteredArray = this.albumArray.filter((element) => {
          return element.genre === value;
        })
      } else {
          return this.filteredArray = this.albumArray
        }
    }
  },
  mounted() {
    setTimeout( () => {
      axios.get('https://flynn.boolean.careers/exercises/api/array/music')
      .then((response) => {
        this.filteredArray = response.data.response;
        this.albumArray = response.data.response;
      });
    }, 500)
  },
}
</script>

<style lang="scss">
@import './assets/scss/style.scss';
</style>
