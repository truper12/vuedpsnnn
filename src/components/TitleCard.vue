<template>
  <article>
    <div class="titlecard">
      <div class="headline">
        <span>공간으로의 이야기,</span>
        <span>단편선</span>
      </div>
      <BookButton />
    </div>
  </article>
</template>

<script>
import BookButton from './BookButton.vue'

export default {
  components: {
    BookButton,
  }
}
</script>

<style scoped>
.titlecard {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.headline {
  color: #F3F1DE;
  display: flex;
  flex-direction: column;
  align-items: center;
}

@media all and (min-width:768px) {
  .titlecard {
    background-image: url('https://static.wixstatic.com/media/7d3d32_b22f15e7350f4ca78b86dd57ec629bfc~mv2.jpg/v1/fill/w_1170,h_1162,al_c,q_85,usm_0.66_1.00_0.01/7d3d32_b22f15e7350f4ca78b86dd57ec629bfc~mv2.webp');
    font-size: 30px;
    padding-top: 20rem;
    padding-bottom: 20rem;
  }
  .headline {
    margin-top: 5rem;
    margin-bottom: 5rem;
  }
}

@media all and (max-width:767px) {
  .titlecard {
    background-image: url('https://static.wixstatic.com/media/7d3d32_b22f15e7350f4ca78b86dd57ec629bfc~mv2.jpg/v1/fill/w_640,h_742,al_c,q_85,usm_0.66_1.00_0.01/7d3d32_b22f15e7350f4ca78b86dd57ec629bfc~mv2.webp');
    background-size: cover;
    font-size: 21px;
    padding-top: 7rem;
    padding-bottom: 7rem;
  }
  .headline {
    margin-top: 3rem;
    margin-bottom: 3rem;
  }
}
</style>
