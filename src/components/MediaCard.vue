<template>
  <article class="mediacard" ref="reff">
    <div class="cardbackmedia">
      <img :src="mobileurl" />
      <!-- <div class="test"> -->
        <video autoplay loop muted :src="desktopurl" type="video/mp4" :style="{transform: `translate3d(0px, ${offset}px, 0px)`}"/>
    <!-- </div> -->
    </div>
    <div class="cardcontent">
      {{ offset }}
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
  },
  methods: {
    handleScroll() {
      // console.log(`scrollY: ${window.scrollY}`)
      // this.offset = window.scrollY * 0.4
      // console.log(this.$refs.reff.getBoundingClientRect().top)
      // this.offset = this.$refs.reff.getBoundingClientRect().top
      var scrollY = window.scrollY
      var innerHeight = window.innerHeight
      var outerHeight = window.outerHeight
      
      // var innerBottom = scrollY+innerHeight
      // var outerBottom = scrollY+outerHeight

      var elementTop = this.$refs.reff.getBoundingClientRect().top
      var elementBottom = this.$refs.reff.getBoundingClientRect().bottom
      console.log(`scrollY: ${scrollY}`)
      console.log(`inner height: ${innerHeight}`)
      console.log(`outer height: ${outerHeight}`)

      console.log(`top: ${elementTop}`)
      console.log(`bottom: ${elementBottom}`)

      console.log(elementTop-innerHeight)
      console.log(elementBottom)

      // console.log((elementTop-innerHeight < 0) ^ (elementBottom < 0))

      console.log('-----')
      if ((elementTop-innerHeight < 0) ^ (elementBottom < 0) > 0) {
        this.offset = elementTop-innerHeight
      }
    }
  },
  mounted() {
    // console.log(window.scrollY)
    window.addEventListener('scroll', this.handleScroll)
  },
  unmounted() {
    window.removeEventListener('scroll', this.handleScroll)
  },
  data() {
    return {
      offset: 0
    }
  }
}
</script>

<style scoped>
/* video {
  transform: translate3d(0px, -0px, 0px);
} */
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
