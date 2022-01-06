<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <Menu />
  <Content />
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Menu from './components/Menu.vue'
import Content from './components/Content.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld
    Menu,
    Content,
  }
}
</script>

<style>
html, body {
  margin: 0;
  padding: 0;
}
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>
