<template lang="pug">
    .overlay-portfolio
        .modal-portfolio
            img(:src="slides.slide" alt="altText").modal-portfolio__img
</template>

<script>
    export default {
        props:['slides']
    }
</script>

<style lang="scss">
    .overlay-portfolio{
        display: flex;
    }
    .modal-portfolio{
        margin: 10% auto;
        &__img{
            max-width: 100%;
        }
    }
</style>
