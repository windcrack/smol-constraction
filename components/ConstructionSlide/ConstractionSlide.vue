<template lang="pug">
    .slide
        img(src="img/constrSlide.png").mask
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss">
    .slide{
        width: 100%;
        overflow: hidden;
        img{
            @media screen and (max-width: 600px){
                object-fit: cover;
                max-width: 100%;
            }
        }

        @media screen and (max-width: 600px){
            width: 320px;
        }
    }
</style>