<template>
  <main>
    <!-- Title -->
    <TitleCard />
    <!-- Intro -->
    <color-card :bgcolor="introcard.bgcolor" :fontcolor="introcard.fontcolor">
      <template v-slot:cardtitle>
        <span v-for="(text, idx) in introcard.cardtitle" :key="{idx}">{{text}}</span>
      </template>
      <template v-slot:cardmain>
        <card-paragraph v-for="(p, idx) in introcard.cardmain" :key="{idx}">
          <template v-slot:cardparagraph>
            <span v-for="(text, j) in p" :key="j">{{text}}</span>
          </template>
        </card-paragraph>
      </template>
    </color-card>
    <!-- Themes -->
    <div v-for="(theme, i) in themes" :key="{i}">
      <media-card
        :mobileurl="theme.mediacard.mobileurl"
        :desktopurl="theme.mediacard.desktopurl">
        <template v-slot:cardcontent>
          <media-card-text v-for="(text, j) in theme.mediacard.text" :key="{j}">
            <template v-slot:text>{{text}}</template>
          </media-card-text>
        </template>
      </media-card>
      <color-card :bgcolor="theme.colorcard.bgcolor" :fontcolor="theme.colorcard.fontcolor">
        <template v-slot:cardtitle>
          <span v-for="(title, j) in theme.colorcard.cardtitle" :key="{j}">{{title}}</span>
        </template>
        <template v-slot:cardmain>
          <card-paragraph v-for="(p, j) in theme.colorcard.cardmain" :key={j}>
            <template v-slot:cardparagraph>
              <span v-for="(text, k) in p" :key="k">{{text}}</span>
            </template>
          </card-paragraph>
        </template>
        <template v-slot:cardbookbutton>
          <book-button :color="theme.colorcard.fontcolor" />
        </template>
      </color-card>
    </div>
    <post-card />
  </main>
</template>

<script>
import TitleCard from './TitleCard.vue'
import ColorCard from './ColorCard.vue'
import CardParagraph from './CardParagraph.vue'
import BookButton from './BookButton.vue'
import MediaCard from './MediaCard.vue'
import MediaCardText from './MediaCardText.vue'
import PostCard from './PostCard.vue'

export default {
  name: 'Content',
  components: {
    TitleCard,
    ColorCard,
    CardParagraph,
    BookButton,
    MediaCard,
    MediaCardText,
    PostCard,
  },
  data() {
    return {
      introcard: {
        bgcolor: 'rgb(2, 52, 63)',
        fontcolor: '#F0EDCC',
        cardtitle: ['Short stories to','feel, live, do.'],
        cardmain: [
          ['우리에게 가장 소중한 경험들이 언제나 그렇듯이,', '단편선에서의 여정은 할 줄의 이야기로부터 시작됩니다.'],
          ['여러분과 저희가 공유하는 이 공간에서, 우리는 함께', '그 이야기를 느끼고, 살고, 써내려가게 됩니다.'],
          ['설레는 마음으로, 언제나 기다리고 있겠습니다.'],
          ['2021년 5월 17일', '단편선 드림']
        ]
      },
      themes: [
        {
          themeid: 1,
          mediacard: {
            mobileurl: 'https://static.wixstatic.com/media/11062b_bd7d32dd41fb42d79843cc0ab9a06e53f000.jpg/v1/fill/w_320,h_132,al_c,q_80,usm_0.33_1.00_0.00/11062b_bd7d32dd41fb42d79843cc0ab9a06e53f000.webp',
            desktopurl: 'https://video.wixstatic.com/video/11062b_bd7d32dd41fb42d79843cc0ab9a06e53/1080p/mp4/file.mp4',
            text: ['첫번째 이야기', '그림자 없는 상자']
          },
          colorcard: {
            bgcolor: '#331B3F',
            fontcolor: '#ACC7B4',
            cardtitle: ['The box with no shadows', '그림자 없는 상자'],
            cardmain: [
              ['미안해 누나. 근데 내가 맞았어. 결국 끝도, 시작도, 누나한테 달렸어.'],
              ['--'],
              ['안다. 비극에 대처하는 방법은 우리 모두 각자 다르다는 것을.', '또한 안다. 어린 나이의 동생에게 막내의 죽음은 감당하기 힘든 일이었을 것이라는 것을.'],
              ['하지만 시현아. 누나도 사람이고, 힘들고, 아파.'],
              ['초자연적인 물체니 뭐니... 동생의 망상을 견뎌주는 것도 이제 한계다.', '지쳐버린 나는 이 허무맹랑한 문자를 받고, 마지막으로 쓴소리를 해주러 시현이의 집으로 향했다.']
            ]
          }
        },
        {
          themeid: 2,
          mediacard: {
            mobileurl: 'https://static.wixstatic.com/media/11062b_00b0cf7d3e8847a4afbde2407008ec49f000.jpg/v1/fill/w_320,h_167,al_c,q_80,usm_0.33_1.00_0.00/11062b_00b0cf7d3e8847a4afbde2407008ec49f000.webp',
            desktopurl: 'https://video.wixstatic.com/video/11062b_00b0cf7d3e8847a4afbde2407008ec49/1080p/mp4/file.mp4',
            text: ['두번째 이야기', '사람들은 그것을 행복이라 부르기로 했다']
          },
          colorcard: {
            bgcolor: 'rgb(106, 123, 162)',
            fontcolor: '#FFDFDE',
            cardtitle: ['We decided to call it happiness', '사람들은 그것을 행복이라 부르기로 했다'],
            cardmain: [
              ['석우는 연기를 들이키며 영원이라는 것에 대해 생각해보았다.','아무래도 불행하겠지, 라고 생각하며 날숨.','영원히 이어지는게 고작 이런 삶이라면, 하며 틱.'],
              ['손을 털며, 그는 오늘의 근무지의 간판을 올려다 보았다.'],
              ['루드베키아.'],
              ['영생을 발명했다는 기묘한 바이오 회사.','공식 발표 이틀 전 사라져버린 연구소장.','그 사건에 배정된 형사, 김석우.'],
              ['석우는 루드베키아의 문을 열었다.']
            ]
          }
        }
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
