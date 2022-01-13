<template>
  <div class="post">
    <div class="postimg">
      <img class="mobile" :src="mobileimg">
      <img class="desktop" :src="desktopimg">
    </div>
    <div class="postcontent">
      <div class="title">
        <slot name="posttitle"></slot>
      </div>
      <div class="text">
        <slot name="posttext"></slot>
      </div>
      <div class="more">
        더 보기
      </div>
      <div class="divider" />
      <div class="playtime">
        <slot name="playtime"></slot>
      </div>
      <div class="button">
        <book-button color="black" />
      </div>
    </div>
  </div>
</template>

<script>
import BookButton from './BookButton.vue'

export default {
  components: {
    BookButton,
  },
  props: {
    mobileimg: { type: String },
    desktopimg: { type: String },
  }
}
</script>

<style scoped>
.post {
  border: 1px solid;
  border-color: rgba(0, 0, 0, 0.2);
  display: flex;
  flex-flow: column wrap;
}

img {
  width: 100%;
}

@media all and (min-width:768px) {
  .post {
    width: 414px;
    height: 716px;
    margin: 2rem;
  }

  .mobile {
    display: none;
  }

  .postimg {
    flex-basis: 0;
    flex-grow: 1.3;
    overflow: hidden;
  }

  .postcontent {
    padding: 31px;
    flex-basis: 0;
    flex-grow: 1;
  }

  .postcontent .title {
    font-size: 20px;
    font-weight: bold;
  }

  .postcontent .text {
    margin-top: 12px;
    margin-bottom: 12px;
  }

  .postcontent .more {
    margin-top: 12px;
    margin-bottom: 12px;
  }

  .postcontent .divider {
    margin-top: 24px;
    margin-bottom: 24px;
    border-bottom: 1px solid rgba(0,0,0, 0.2);
  }

  .postcontent .playtime {
    font-size: 16px;
    margin-bottom: 20px;
  }
}

@media all and (max-width:767px) {
  .post {
    width: 280px;
    height: 435px;
    margin: 1.5rem;
  }

  .desktop {
    display: none;
  }

  .postimg {
    flex-basis: 0;
    flex-grow: 1;
    overflow: hidden;
  }

  .postcontent {
    padding: 20px;
    flex-basis: 0;
    flex-grow: 1.3;
  }

  .postcontent .title {
    font-size: 20px;
    font-weight: bold;
  }

  .postcontent .text {
    margin-top: 12px;
    margin-bottom: 12px;
  }

  .postcontent .more {
    margin-top: 12px;
    margin-bottom: 12px;
  }

  .postcontent .divider {
    margin-top: 16px;
    margin-bottom: 16px;
    border-bottom: 1px solid rgba(0,0,0, 0.2);
  }

  .postcontent .playtime {
    font-size: 14px;
    margin-bottom: 20px;
  }
}
</style>
