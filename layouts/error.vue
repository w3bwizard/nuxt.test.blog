<template>
  <section>
    <h1>Error 404</h1>
    <h2>Page not found</h2>
    <nuxt-link to="/">Go home</nuxt-link>
  </section>
</template>

<style scoped>
  h1 {
    font-weight: bolder;
    color: brown;
    font-size: 38px;
  }
  h2 {
    font-size: 16px;
  }
  section {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 400px;
    height: 400px;
    
    margin: 0 auto;
  }
</style>