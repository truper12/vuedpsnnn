<template>
  <article class="colorcard" :style="{ 'background-color': bgcolor, 'color': fontcolor}">
    <div class="cardtitle">
      <slot name="cardtitle"></slot>
    </div>
    <div class="cardmain">
      <slot name="cardmain"></slot>
    </div>
    <div class="cardbookbutton">
      <slot name="cardbookbutton"></slot>
    </div>
  </article>
</template>

<script>
// import BookButton from './BookButton.vue'

export default {
  components: {
    // BookButton,
  },
  props: {
    bgcolor: { type: String },
    fontcolor: { type: String },
  }
}
</script>

<style scoped>
.colorcard {
  display: flex;
  flex-direction: column;
  /* color: #F0EDCC; */
}

.cardtitle {
  display: flex;
  flex-direction: column;
  width: 100%;
}

.cardmain {
  width: 100%;
}

@media all and (min-width:768px) {
  .colorcard {
    padding-top: 7rem;
    padding-bottom: 7rem;
    padding-left: 7rem;
    padding-right: 7rem;
  }

  .cardtitle {
    font-size: 40px;
    font-weight: bold;
    margin-bottom: 4rem;
  }

  .cardbookbutton {
    margin-top: 4rem;
  }
}

@media all and (max-width:767px) {
  .colorcard {
    padding-top: 3rem;
    padding-bottom: 3rem;
    padding-left: 1rem;
    padding-right: 1rem;
    align-items: center;
  }
  
  .cardtitle {
    font-size: 24px;
    font-weight: bold;
    margin-bottom: 2rem;
  }

  .cardbookbutton {
    margin-top: 1rem;
  }
}
</style>
