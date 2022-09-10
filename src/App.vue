<template>
  <div id="app">
    <HeaderComponent @findGenre="onGenre"/>
    <MainComponent :genre="searchGenre"/>
  </div>
</template>

<script>
  import HeaderComponent from './components/HeaderComponent.vue';
  import MainComponent from './components/MainComponent.vue';

export default {
  name: 'App',
  data() {
    return {
      searchGenre: '',
    }
  },
  components: {
      MainComponent,
      HeaderComponent,
  },
  methods: {
    onGenre(data) {
      this.searchGenre = data;
      console.log('Ascolto l evento "findGenre"',data)
    }
  }
}
</script>

<style lang="scss">
  @import "./styles/general.scss";
</style>
