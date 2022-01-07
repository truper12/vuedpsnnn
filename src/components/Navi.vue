<template>
  <nav>
    <ul>
      <li>menu 1</li>
      <li>menu 2</li>
      <li>menu 3</li>
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
  }

  ul{
    list-style-type: none;
    display: flex;
  }
}

@media all and (max-width:767px) {
  nav {
    display: none;
  }
}
</style>
