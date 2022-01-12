<template>
  <div class="cardparagraph">
    <slot name="pcontent"></slot>
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
    margin-bottom: 1rem
  }
}

@media all and (max-width:767px) {
  .cardparagraph {
    font-size: 12px;
    margin-bottom: 1rem
  }
}
</style>
