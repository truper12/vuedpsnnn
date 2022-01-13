<template>
  <article class="postcard">
    <post />
    <post />
  </article>
</template>

<script>
import Post from './Post.vue'

export default {
  components: {
    Post
  },
}
</script>

<style scoped>
.postcard {
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
}

@media all and (min-width:768px) {

}

@media all and (max-width:767px) {

}
</style>
