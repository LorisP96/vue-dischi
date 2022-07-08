<template>
  <div id="app">
    <HeaderComponents />
    <main>
      <MainComponents />
    </main>
  </div>
</template>

<script>
import HeaderComponents from './components/HeaderComponents.vue';
import MainComponents from './components/MainComponents.vue';


export default {
  name: 'App',
  components: {
    HeaderComponents,
    MainComponents
  }
}
</script>

<style lang="scss">
@import './assets/scss/style.scss';
</style>
