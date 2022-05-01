<template>
project
        <h2>{{project.name}}</h2>
        <p>{{project.text}}</p>
</template>

<script>
    import projects from '@/content/data'
    export default {
        name: 'single',
        data() {
            return {
                project: []
            }
        },

        mounted() {
            // find the project in the projects array
            this.project = projects.find(project => project.slug === this.$route.params.slug)

            // if the project is not found, redirect to 404
            if (!this.project) {
                this.$router.push('/404')
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
      height: 100vh;
  }

</style>