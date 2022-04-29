<template>
    <div class="start-middle">
        <img src="@/assets/images/nicolas-de-garrigues.webp" alt="Photo de Nicolas de Garrigues" width="800">
        <article>
            <h3>Your</h3>
            <h1>Fullstack</h1>
            <h2>Developer</h2>
        </article>
    </div>
</template>
<script>
    export default {
        name: 'middle'
    }
</script>
<style>
    .start-middle {
        position: relative;
        display: flex;
        justify-content: center;
        align-items: center;
        text-transform: uppercase;
    }

    .start-middle img {
        position: absolute;
        top: -10vh;
        left: 15%;
        transform: scaleX(-1);
    }

    .start-middle article {
        position: absolute;
        right: 20%;
        top: 20vh;
        text-align: justify;
    }

    .start-middle article h1 {
        letter-spacing: 10px;
        font-size: 6em;
        font-weight: bold;
        margin-bottom: 20px;
    }

    .start-middle article h2 {
        letter-spacing: 30px;
        font-size: 4em;
        font-style: italic;
        color: rgba(255, 255, 255, 0.6);
        font-weight: lighter;

    }

    .start-middle article h3 {
        letter-spacing: 50px;
        font-size: 3em;
        font-weight: lighter;
        margin-bottom: 20px;
    }
</style>