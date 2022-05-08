<template>
    <NuxtLayout name="app-layout">
      <Start id="start" class="start" />
      <About id="about" class="about" />
      <Skills id="skills" class="skills" />
    </NuxtLayout>
</template>

<script>
  import AOS from '@/mixins/aos'
  export default {
    name: 'index',
    mixins: [
      AOS,
    ]
  }
</script>

<style>
  /* reset */
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
    scroll-behavior: smooth;
  }
  
  h1, h2, h3, h4, h5, h6 {
    font-weight: normal;
    font-size: 1em;
  }

  /* base */
  body {
    overflow-x: hidden;
    background: #161616;
    color: #ffffff;
    font-family: 'Lato', sans-serif;
  }

  .start, .about, .skills {
    height: 100vh;
  }

</style>