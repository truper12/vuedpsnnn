<template>
  <article>
    <div class="introcard" :style="{ 'background-color': color }">
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
  },
  props: {
    color: { type: String }
  }
  
}
</script>

<style scoped>
.introcard {
  display: flex;
  flex-direction: column;
  /* background-color: rgb(2, 52, 63); */
  color: #F0EDCC;
}

.cardtitle {
  display: flex;
  flex-direction: column;
}

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
</style>
