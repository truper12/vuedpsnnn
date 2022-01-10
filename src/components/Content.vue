<template>
  <main>
    <TitleCard />
    <IntroCard />
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
import IntroCard from './IntroCard.vue'

export default {
  name: 'Content',
  components: {
    // HelloWorld
    Card,
    TitleCard,
    IntroCard,
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
