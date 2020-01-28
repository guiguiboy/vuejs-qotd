<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Menu/>

    <QotdList name="Latest first" :pagination="false" :limit="10" sortColumn="date" sortOrder="desc">
    </QotdList>

  </div>
</template>

<script>
import Menu from './components/Menu.vue'
import QotdList from "./components/QotdList";

export default {
  name: 'app',
  components: {
    QotdList,
    Menu
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
