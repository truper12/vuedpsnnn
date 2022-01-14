<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <Header />
  <Content />
  <Footer />
</template>

<script>
import Header from './components/Header.vue'
import Content from './components/Content.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Content,
    Footer,
  }
}
</script>

<style>
@font-face {
  font-family: 'Noto Serif KR', serif;
  src: url('https://fonts.googleapis.com/css2?family=Noto+Serif+KR:wght@600&display=swap');
}
/* @import url('https://fonts.googleapis.com/css2?family=Noto+Serif+KR:wght@600&display=swap'); */
html, body {
  margin: 0;
  padding: 0;
}
#app {
  font-family: 'Noto Serif KR', serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
