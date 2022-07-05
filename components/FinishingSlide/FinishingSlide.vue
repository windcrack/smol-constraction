<template lang="pug">
    .finishing-slide
        img(:src="img").finishing-slide__img.mask
</template>

<script>
    export default {
        props: ['img']
    }
</script>

<style lang="scss">
    .finishing-slide{
        overflow: hidden;

        &__img{
            object-fit: cover;
            @media (max-width: 1200px){
                object-fit: cover;
                max-width: 100%;

            }
        }

        // @media (max-width: 1200px){
        //     width: 714px;
        // }

        @media (max-width: 600px){
            width: 320px;
        }
    }
</style>