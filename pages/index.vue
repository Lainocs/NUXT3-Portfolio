<template>
    <NuxtLayout name="app-layout">
      <Start class="start" />
    </NuxtLayout>
</template>

<script>
  export default {
    name: 'index',
  }
</script>

<style>
  /* reset */
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  
  h1, h2, h3, h4, h5, h6 {
    font-weight: normal;
    font-size: 1em;
  }

  /* base */
  body {
    background: #000000;
    color: #ffffff;
    font-family: 'Lato', sans-serif;
  }

  .start {
      height: 100vh;
  }

</style>