<template>
  <div id="app">
    <h1>API Data Fetcher</h1>
    <ApiData />
  </div>
</template>

<script>
import ApiData from './components/APIData.vue';

export default {
  name: 'App',
  components: {
    ApiData
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  margin-top: 40px;
}
</style>
