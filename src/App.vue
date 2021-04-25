<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <DataTable />
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import DataTable from "./components/DataTable.vue";

export default {
  name: "App",
  components: {
    // HelloWorld
    DataTable,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
