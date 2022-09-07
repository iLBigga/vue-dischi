<template>
  <div id="app">
    <HeaderComponent/>
    <MainComponent/>
  </div>
</template>

<script>
  import HeaderComponent from './components/HeaderComponent.vue';
  import MainComponent from './components/MainComponent.vue';

export default {
  name: 'App',
  components: {
      MainComponent,
      HeaderComponent,
  }
}
</script>

<style lang="scss">
  @import "./styles/general.scss";
</style>
