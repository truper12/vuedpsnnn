<template>
  <article class="postcard">
    <slot name="postcard"></slot>
  </article>
</template>

<script>
export default {
  components: {
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
