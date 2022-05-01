<template>
    <div class="start-scroll">
        <span>Scroll down</span>
        <img src="@/assets/images/scroll/arrow.png" alt="Arrow" width="20">
    </div>
</template>
<script>
    export default {
        name: 'scroll',
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
    }

    @media screen and (max-width: 1000px) {
        .start-scroll {
            right: 0;
            align-items: flex-start;
            gap: 0;
        }
    }
</style>