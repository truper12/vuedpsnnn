<template>
  <span>
    <slot name="text"></slot>
  </span>
</template>

<script>
export default {
}
</script>

<style scoped>

@media all and (min-width:768px) {
  span {
    font-size: 40px;
    font-weight: bold;
    margin-bottom: 1rem;
  }
  
}

@media all and (max-width:767px) {
  span {
    font-size: 21px;
    font-weight: bold;
    margin-bottom: 1rem;
  }
}
</style>
