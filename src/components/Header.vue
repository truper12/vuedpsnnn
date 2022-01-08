<template>
  <header>
    <div class="title">
      dpsnnn
    </div>
    <Navi />
  </header>
</template>

<script>
import Navi from './Navi.vue'

export default {
  components: {
    Navi,
  }
}
</script>

<style scoped>
header {
  /* padding-top: 0.5rem;
  padding-bottom: 0.5rem; */
  margin-top: 1.5rem;
  margin-bottom: 1.5rem;
  display: flex;
  align-items: center;
  background: transparent;
}


/* @media all and (min-width:1024px) {
   ... 
}

@media all and (min-width:768px) and (max-width:1023px) {
   ...
} */

@media all and (min-width:768px) {
  header {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    justify-content: space-between;
    /* justify-content: space-around; */
    padding-left: 3.5rem;
    padding-right: 5rem;
    background-color: transparent;
  }

  .title {
    font-size: 30px;
    color: #F3F1DE;
  }
}

@media all and (max-width:767px) {
  header {
    justify-content: center;
  }

  .title {
    font-size: 20px;
    color: rgba(106,123,162,1);
  }
}
</style>
