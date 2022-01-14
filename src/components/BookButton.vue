<template>
  <button :style="{ 'color': color, 'border-color': color}">
    예약하기
  </button>
</template>

<script>
export default {
  props: {
    color: { type: String, default: 'white' },
  }
}
</script>

<style scoped>

button {
  font-family: 'Noto Serif KR', serif;
  background-color: transparent;
}

@media all and (min-width:768px) {
  button {
    font-size: 20px;
    border: 2px solid;
    padding-left: 7rem;
    padding-right: 7rem;
    padding-top: 2rem;
    padding-bottom: 2rem;
  }
}

@media all and (max-width:767px) {
  button {
    font-size: 14px;
    border: 1px solid;
    padding-left: 3rem;
    padding-right: 3rem;
    padding-top: 1rem;
    padding-bottom: 1rem;
  }
}
</style>
