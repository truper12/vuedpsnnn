<template>
  <footer>
    <span>We are, as a species, addicted to stories</span>
  </footer>
</template>

<script>
export default {
  components: {
  }
}
</script>

<style scoped>
footer {
  display: flex;
  flex-direction: column;
  align-items: center;
}

footer span {
  color: #757575;
}

@media all and (min-width:768px) {
  footer span {
    font-size: 15px;
  }
}

@media all and (max-width:767px) {
  footer {
    padding-top: 0.65rem;
    padding-bottom: 1.9rem;
  }
  footer span {
    font-size: 16px;
  }
}
</style>
