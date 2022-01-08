<template>
  <nav>
    <ul>
      <li>단편선</li>
      <li>예약하기</li>
      <li>첫번째 이야기</li>
      <li>두번째 이야기</li>
      <li>Plans & Pricing</li>
    </ul>
  </nav>
</template>

<script>
export default {
  
}
</script>

<style scoped>


@media all and (min-width:768px) {
  nav {
    display: flex;
    flex-wrap: wrap;
    color: #F3F1DE;
  }

  ul {
    list-style-type: none;
    display: flex;
  }

  li {
    margin-left: 1rem;
    margin-right: 1rem;
  }
}

@media all and (max-width:767px) {
  nav {
    display: none;
  }
}
</style>
