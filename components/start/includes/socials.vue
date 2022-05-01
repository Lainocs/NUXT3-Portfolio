<template>
    <div class="start-socials">
        <img src="@/assets/images/socials/github.png" alt="Logo GitHub" width="30">
        <img src="@/assets/images/socials/linkedin.png" alt="Logo Linkedin" width="30">
    </div>
</template>
<script>
    export default {
        name: 'socials',
    }
</script>
<style>
    .start-socials {
        display: flex;
        gap: 30px;
        position: absolute;
        top: 50%;
        left: 2%;
        width: fit-content;
        transform: rotate(-90deg);
    }

    @media screen and (max-width: 1000px) {
        .start-socials {
            transform: rotate(0deg);
            top: 80vh;
            left: 10vw;
        }
    }
</style>