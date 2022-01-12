<template>
  <div class="cardparagraph">
    <slot name="cardparagraph"></slot>
  </div>
</template>

<script>
export default {
}
</script>

<style scoped>
.cardparagraph {
  display: flex;
  flex-direction: column;
}

@media all and (min-width:768px) {
  .cardparagraph {
    font-size: 20px;
    margin-bottom: 1em
  }
}

@media all and (max-width:767px) {
  .cardparagraph {
    font-size: 12px;
    margin-bottom: 1em
  }
}
</style>
