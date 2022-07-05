<template lang="pug">
    .portfolio-typical-slide
        img(:src="pti").portfolio-typical-slide__img
</template>

<script>
    export default {
        props:['pti']
    }
</script>

<style lang="scss">
    .portfolio-typical-slide{
        display: flex;
        justify-content: center;
        // width: 920px;

        @media (max-width: 1200px){
            width: 520px;
            height: 237px;
        }

        @media (max-width: 600px){
            width: 285px;
            height: 130px;
        }

        &__img{
            display: block;
            @media (max-width: 1200px){
                max-width: 100%;
                height: auto;
            }

            @media (max-width: 600px){
                max-width: 100%;
                height: auto;
            }
        }
    }
</style>