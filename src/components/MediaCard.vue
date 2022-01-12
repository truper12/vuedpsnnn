<template>
  <article class="mediacard">
    <div class="cardbackmedia">
      <img :src="mobileurl" />
      <video autoplay loop :src="desktopurl" type="video/mp4" />
    </div>
    <div class="cardcontent">
      <slot name="cardcontent"></slot>
    </div>
  </article>
</template>

<script>
export default {
  components: {
  },
  props: {
    mobileurl: { type: String },
    desktopurl: { type: String },
  }
}
</script>

<style scoped>
.mediacard {
  position: relative;
  overflow: hidden;
}

.cardbackmedia {
  position: absolute;
  z-index: -1;
}

.cardcontent {
  /* width: 100%; */

  display: flex;
  flex-direction: column;
  align-items: center;

  color: #F3F1DE;
}

@media all and (min-width:768px) {
  video {
    object-fit: cover;
  }

  img {
    display: none;
  }

  .cardcontent {
    padding-top: 10rem;
    padding-bottom: 10rem;
  }
}

@media all and (max-width:767px) {
  video {
    display: none;
  }

  .cardbackmedia {
    left: 0;
    right: 0;
  }

  img {
    width: 100%;
  }
  
  .cardcontent {
    padding-top: 3rem;
    padding-bottom: 2rem;
  }
}
</style>
