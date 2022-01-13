<template>
  <div class="post">
    <div class="postimg">
      <img class="mobile" src="https://static.wixstatic.com/media/7d3d32_fb2337143586484b8ba78480ab1e76eb~mv2.jpg/v1/fill/w_556,h_367,fp_0.50_0.50,q_80,usm_0.66_1.00_0.01/7d3d32_fb2337143586484b8ba78480ab1e76eb~mv2.webp">
      <img class="desktop" src="https://static.wixstatic.com/media/7d3d32_fb2337143586484b8ba78480ab1e76eb~mv2.jpg/v1/fill/w_825,h_825,fp_0.50_0.50,q_85,usm_0.66_1.00_0.01/7d3d32_fb2337143586484b8ba78480ab1e76eb~mv2.webp">
    </div>
    <div class="postcontent">
      <div class="title">
        그림자 없는 상자
      </div>
      <div class="text">
        "결국 끝도, 시작도, 누나한테 달렸어."
      </div>
      <div class="more">
        더 보기
      </div>
      <div class="divider" />
      <div class="playtime">
        1 hr 10 min
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
