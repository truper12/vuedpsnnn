<template>
  <article>
    <div class="introcard">
      <div class="cardtitle">
        <span>Short stories to</span>
        <span>feel, live, do.</span>
      </div>
      <div class="cardmain">
        <div class="cardparagraph">
          <span>우리에게 가장 소중한 경험들이 언제나 그렇듯이,</span>
          <span>단편선에서의 여정은 할 줄의 이야기로부터 시작됩니다.</span>
        </div>
        <div class="cardparagraph">
          <span>여러분과 저희가 공유하는 이 공간에서, 우리는 함께</span>
          <span>그 이야기를 느끼고, 살고, 써내려가게 됩니다.</span>
        </div>
        <div class="cardparagraph">
          <span>설레는 마음으로, 언제나 기다리고 있겠습니다.</span>
        </div>
        <div class="cardparagraph">
          <span>2021년 5월 17일,</span>
          <span>단편선 드림</span>
        </div>
      </div>
      <!-- <BookButton /> -->
    </div>
  </article>
</template>

<script>
// import BookButton from './BookButton.vue'

export default {
  components: {
    // BookButton,
  }
}
</script>

<style scoped>
.introcard {
  display: flex;
  flex-direction: column;
  background-color: rgb(2, 52, 63);
  color: #F0EDCC;
}

.cardtitle {
  display: flex;
  flex-direction: column;
}

/* .cardmain {
  display: flex;
  flex-direction: column;
} */

.cardparagraph {
  display: flex;
  flex-direction: column;
}

@media all and (min-width:768px) {
  .introcard {
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

  .cardparagraph {
    font-size: 20px;
    margin-bottom: 1rem
  }
}

@media all and (max-width:767px) {
  .introcard {
    padding-top: 3rem;
    padding-bottom: 3rem;
    padding-left: 1rem;
    padding-right: 1rem;
  }
  
  .cardtitle {
    font-size: 24px;
    font-weight: bold;
    margin-bottom: 2rem;
  }

  .cardparagraph {
    font-size: 12px;
    margin-bottom: 1rem
  }
}
/* .titlecard {
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
} */
</style>
