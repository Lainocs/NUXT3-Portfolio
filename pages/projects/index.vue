<template>
    <div v-for="project in projects" :key="project.slug">
        <h2>{{project.name}}</h2>
        <p>{{project.text}}</p>
        <a :href="'/projects/' + project.slug">Voir le project</a>
    </div>
</template>

<script>
  import projects from '@/content/data.json'
  export default {
    name: 'index',
    data() {
        return {
            projects: projects
        }
    },
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
      height: 90vh;
  }

</style>