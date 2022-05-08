<template>
    <div class="start-middle">
        <img src="@/assets/images/nicolas-de-garrigues.webp" alt="Photo de Nicolas de Garrigues" data-aos="zoom-in" data-aos-delay="100" data-aos-duration="1000">
        <article data-aos="fade-left" data-aos-delay="500" data-aos-duration="1000">
            <h3>Your</h3>
            <h1>Fullstack</h1>
            <h2>Developer</h2>
        </article>
    </div>
</template>
<script>
    import AOS from '@/mixins/aos'
    export default {
        name: 'middle',
        mixins: [
            AOS
        ]
    }
</script>
<style>
    .start-middle {
        height: 90vh;
        margin: 0 auto;
        position: relative;
        display: flex;
        justify-content: center;
        align-items: center;
        text-transform: uppercase;
    }

    .start-middle img {
        width: 30%;
        position: absolute;
        left: 25%;
        transform: scaleX(-1) translate(0);
    }

    .start-middle article {
        position: absolute;
        right: 20%;
    }

    .start-middle article h1 {
        letter-spacing: 10px;
        font-size: 4vw;
        font-weight: bold;
        margin-bottom: 20px;
    }

    .start-middle article h2 {
        letter-spacing: 30px;
        font-size: 3vw;
        font-style: italic;
        color: rgba(255, 255, 255, 0.6);
        font-weight: lighter;

    }

    .start-middle article h3 {
        letter-spacing: 50px;
        font-size: 2vw;
        font-weight: lighter;
        margin-bottom: 20px;
    }

    @media screen and (max-width: 1000px) {
        .start-middle {
            top: -10vh;
        }
        .start-middle img {
            position: initial;
            transform: scaleX(-1) translate(0);
            width: 50%;
            opacity: 0.5;
        }

        .start-middle article {
            /* position: initial; */
            top: 50%;
            left: 20%;
            transform: translate(50%, 50%);
        }
    }
</style>