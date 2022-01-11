<template>
  <article class="mediacard">
    <div class="cardbackmedia">
      <img src="https://static.wixstatic.com/media/11062b_bd7d32dd41fb42d79843cc0ab9a06e53f000.jpg/v1/fill/w_320,h_132,al_c,q_80,usm_0.33_1.00_0.00/11062b_bd7d32dd41fb42d79843cc0ab9a06e53f000.webp" />
      <video autoplay loop src="https://video.wixstatic.com/video/11062b_bd7d32dd41fb42d79843cc0ab9a06e53/1080p/mp4/file.mp4" type="video/mp4" />
    </div>
    <div class="cardcontent">
      <span>첫번째 이야기</span>
      <span>그림자 없는 상자</span>
    </div>
  </article>
</template>

<script>
export default {
  components: {
  }
}
</script>

<style scoped>
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

  .cardcontent span {
    font-size: 40px;
    font-weight: bold;
    margin-bottom: 1rem;
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

  .cardcontent span {
    font-size: 21px;
    font-weight: bold;
    margin-bottom: 1rem;
  }
}
</style>
