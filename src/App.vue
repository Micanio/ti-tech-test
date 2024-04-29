<template>
  <Header />
  <Bundle />
</template>

<script>
import Header from './components/Header.vue';
import Bundle from './components/Bundle.vue';


export default {
  name: 'App',
  components: {
    Header,
    Bundle
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
