<template>
  <main>
    <TitleCard />
    <color-card bgcolor="rgb(2, 52, 63)" fontcolor="#F0EDCC">
      <template v-slot:cardtitle>
        <span>Short stories to</span>
        <span>feel, live, do.</span>
      </template>
      <template v-slot:cardmain>
        <card-paragraph>
          <template v-slot:cardparagraph>
            <span>우리에게 가장 소중한 경험들이 언제나 그렇듯이,</span>
            <span>단편선에서의 여정은 할 줄의 이야기로부터 시작됩니다.</span>
          </template>
        </card-paragraph>
        <card-paragraph>
          <template v-slot:cardparagraph>
            <span>여러분과 저희가 공유하는 이 공간에서, 우리는 함께</span>
            <span>그 이야기를 느끼고, 살고, 써내려가게 됩니다.</span>
          </template>
        </card-paragraph>
        <card-paragraph>
          <template v-slot:cardparagraph>
            <span>설레는 마음으로, 언제나 기다리고 있겠습니다.</span>
          </template>
        </card-paragraph>
        <card-paragraph>
          <template v-slot:cardparagraph>
            <span>2021년 5월 17일,</span>
            <span>단편선 드림</span>
          </template>
        </card-paragraph>
      </template>
    </color-card>
    <media-card
      mobileurl="https://static.wixstatic.com/media/11062b_bd7d32dd41fb42d79843cc0ab9a06e53f000.jpg/v1/fill/w_320,h_132,al_c,q_80,usm_0.33_1.00_0.00/11062b_bd7d32dd41fb42d79843cc0ab9a06e53f000.webp"
      desktopurl="https://video.wixstatic.com/video/11062b_bd7d32dd41fb42d79843cc0ab9a06e53/1080p/mp4/file.mp4">
      <template v-slot:cardcontent>
        <media-card-text>
          <template v-slot:text>첫번째 이야기</template>
        </media-card-text>
        <media-card-text>
          <template v-slot:text>그림자 없는 상자</template>
        </media-card-text>
      </template>
    </media-card>
    <color-card bgcolor="#331B3F" fontcolor="#ACC7B4">
      <template v-slot:cardtitle>
        <span>The box with no shadows</span>
        <span>그림자 없는 상자</span>
      </template>
      <template v-slot:cardmain>
        <card-paragraph>
          <template v-slot:cardparagraph>
            <span>"미안해 누나. 근데 내가 맞았어. 결국 끝도, 시작도, 누나한테 달렸어."</span>
          </template>
        </card-paragraph>
        <card-paragraph>
          <template v-slot:cardparagraph>
            <span>--</span>
          </template>
        </card-paragraph>
        <card-paragraph>
          <template v-slot:cardparagraph>
            <span>안다. 비극에 대처하는 방법은 우리 모두 각자 다르다는 것을.</span>
            <span>또한 안다. 어린 나이의 동생에게 막내의 죽음은 감당하기 힘든 일이었을 것이라는 것을.</span>
          </template>
        </card-paragraph>
        <card-paragraph>
          <template v-slot:cardparagraph>
            <span>하지만 시현아. 누나도 사람이고, 힘들고, 아파.</span>
          </template>
        </card-paragraph>
        <card-paragraph>
          <template v-slot:cardparagraph>
            <span>초자연적인 물체니 뭐니... 동생의 망상을 견뎌주는 것도 이제 한계다.</span>
            <span>지쳐버린 나는 이 허무맹랑한 문자를 받고, 마지막으로 쓴소리를 해주러 시현이의 집으로 향했다.</span>
          </template>
        </card-paragraph>
      </template>
      <template v-slot:cardbookbutton>
        <book-button color="#ACC7B4" />
      </template>
    </color-card>
    <media-card
      mobileurl="https://static.wixstatic.com/media/11062b_00b0cf7d3e8847a4afbde2407008ec49f000.jpg/v1/fill/w_320,h_167,al_c,q_80,usm_0.33_1.00_0.00/11062b_00b0cf7d3e8847a4afbde2407008ec49f000.webp"
      desktopurl="https://video.wixstatic.com/video/11062b_00b0cf7d3e8847a4afbde2407008ec49/1080p/mp4/file.mp4">
      <template v-slot:cardcontent>
        <media-card-text>
          <template v-slot:text>두번째 이야기</template>
        </media-card-text>
        <media-card-text>
          <template v-slot:text>사람들은 그것을 행복이라 부르기로 했다</template>
        </media-card-text>
      </template>
    </media-card>
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
import ColorCard from './ColorCard.vue'
import CardParagraph from './CardParagraph.vue'
import BookButton from './BookButton.vue'
import MediaCard from './MediaCard.vue'
import MediaCardText from './MediaCardText.vue'

export default {
  name: 'Content',
  components: {
    // HelloWorld
    Card,
    TitleCard,
    ColorCard,
    CardParagraph,
    BookButton,
    MediaCard,
    MediaCardText,
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
