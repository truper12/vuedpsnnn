<template>
  <main>
    <TitleCard />
    <!-- <IntroCard /> -->
    <color-card bgcolor="rgb(2, 52, 63)" fontcolor="#F0EDCC">
      <template v-slot:cardtitle>
        <span>Short stories to</span>
        <span>feel, live, do.</span>
      </template>
      <template v-slot:cardparagraph>
        <card-paragraph>
          <template v-slot:pcontent>
            <span>우리에게 가장 소중한 경험들이 언제나 그렇듯이,</span>
            <span>단편선에서의 여정은 할 줄의 이야기로부터 시작됩니다.</span>
          </template>
        </card-paragraph>
        <card-paragraph>
          <template v-slot:pcontent>
            <span>여러분과 저희가 공유하는 이 공간에서, 우리는 함께</span>
            <span>그 이야기를 느끼고, 살고, 써내려가게 됩니다.</span>
          </template>
        </card-paragraph>
        <card-paragraph>
          <template v-slot:pcontent>
            <span>설레는 마음으로, 언제나 기다리고 있겠습니다.</span>
          </template>
        </card-paragraph>
        <card-paragraph>
          <template v-slot:pcontent>
            <span>2021년 5월 17일,</span>
            <span>단편선 드림</span>
          </template>
        </card-paragraph>
      </template>
    </color-card>
    <theme-title-card />
    <color-card bgcolor="#331B3F" fontcolor="#ACC7B4">
      <template v-slot:cardtitle>
        <span>The box with no shadows</span>
        <span>그림자 없는 상자</span>
      </template>
      <template v-slot:cardparagraph>
        <card-paragraph>
          <template v-slot:pcontent>
            <span>"미안해 누나. 근데 내가 맞았어. 결국 끝도, 시작도, 누나한테 달렸어."</span>
          </template>
        </card-paragraph>
        <card-paragraph>
          <template v-slot:pcontent>
            <span>--</span>
          </template>
        </card-paragraph>
        <card-paragraph>
          <template v-slot:pcontent>
            <span>안다. 비극에 대처하는 방법은 우리 모두 각자 다르다는 것을.</span>
            <span>또한 안다. 어린 나이의 동생에게 막내의 죽음은 감당하기 힘든 일이었을 것이라는 것을.</span>
          </template>
        </card-paragraph>
        <card-paragraph>
          <template v-slot:pcontent>
            <span>초자연적인 물체니 뭐니... 동생의 망상을 견뎌주는 것도 이제 한계다.</span>
            <span>지쳐버린 나는 이 허무맹랑한 문자를 받고, 마지막으로 쓴소리를 해주러 시현이의 집으로 향했다.</span>
          </template>
        </card-paragraph>
      </template>
      <template v-slot:cardbookbutton>
        <book-button color="#ACC7B4" />
      </template>
    </color-card>
    This is Content
    <!-- <Card cardtype="blue" />
    <Card cardtype="purple" /> -->
    <Card v-for="(card, idx) in cards" :key="{idx}" :item="card" />
    <!-- <Card :items="cards" /> -->
  </main>
</template>

<script>
import Card from './Card.vue'
import TitleCard from './TitleCard.vue'
// import IntroCard from './IntroCard.vue'
import ThemeTitleCard from './ThemeTitleCard.vue'
import ColorCard from './ColorCard.vue'
import CardParagraph from './CardParagraph.vue'
import BookButton from './BookButton.vue'

export default {
  name: 'Content',
  components: {
    // HelloWorld
    Card,
    TitleCard,
    // IntroCard,
    ThemeTitleCard,
    ColorCard,
    CardParagraph,
    BookButton
  },
  data() {
    return {
      cards: [
        {
          cardtype: 'blue',
          imgurl: ''
        },
        {
          cardtype: 'purple',
          imgurl: ''
        },
        // {
        //   cardtype: 'img',
        //   imgurl: 'http://t1.daumcdn.net/cartoon/5913FCAC0234C50001'
        // }
      ]
    }
  }
}
</script>

<style scoped>
main {
  width: 100%;
  display: block;
}
</style>
