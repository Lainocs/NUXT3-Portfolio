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