<template>
    <div class="header">
        <div class="header-title">
            <h2>Nicolas de Garrigues</h2>
        </div>
        <Navbar />
    </div>
</template>
<script>
    import Navbar from "./navbar.vue";
    export default {
    name: "includes-header",
    components: { Navbar }
}
</script>

<style>
    .header {
        height: 10vh;
        padding: 0 50px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        text-transform: uppercase;
    }

    .header-title {
        font-size: 1.5em;
        font-weight: bold;
    }
</style>