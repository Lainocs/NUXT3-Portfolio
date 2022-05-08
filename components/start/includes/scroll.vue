<template>
    <a class="start-scroll" href="#about">
        <span>Scroll down</span>
        <img src="@/assets/images/scroll/arrow.png" alt="Arrow" width="20" data-aos="fade-left" data-aos-delay="1000" data-aos-duration="1000">
    </a>
</template>
<script>
    import AOS from '@/mixins/aos'
    export default {
        name: 'scroll',
        mixins: [
            AOS
        ]
    }
</script>
<style>
    .start-scroll {
        font-size: 0.8em;
        text-transform: uppercase;
        letter-spacing: 5px;
        display: flex;
        align-items: center;
        gap: 30px;
        position: absolute;
        bottom: 15%;
        right: 0%;
        transform: rotate(90deg);
        cursor: pointer;
        color: #fff;
        text-decoration: none;
    }

    @media screen and (max-width: 1000px) {
        .start-scroll {
            right: 0;
            align-items: flex-start;
            gap: 0;
        }
    }
</style>