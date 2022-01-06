<template>
  <!-- <article v-bind:class="['card', cardtype]">
    This is Card
  </article> -->
  <article> <!-- v-for="(item, idx) in items" :key="{idx}"> -->
    <div :class="item.cardtype" :style="{ 'background-image': `url(${item.imgurl})` }">
      This is Card
      <!-- <img v-if="item.imgurl" :src="item.imgurl" /> -->
    </div>
  </article>
</template>

<script>
export default {
  props: {
    // cardtype: { type: String, default: '' },
    // items: { type: Array, default: () => [] }
    item: { type: Object, default: null }
  }
}
</script>

<style scoped>
.card {
  border: 0;
}
.blue {
  background: #009bff;
}
.purple {
  background: #8f46ff;
}
.green {
  background: #00bcac;
}
.img {
  background: transparent;
  width: 500px;
  height: 500px;
}
</style>
