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