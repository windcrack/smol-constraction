<template lang="pug">
    .overlay-reviews
        .modal-reviews
            img(:src="slides.slide" alt="altText").modal-reviews__img
</template>

<script>
    export default {
        props:['slides'],
    }
</script>

<style lang="scss">
    .overlay-reviews{
        display: flex;
    }

    .modal-reviews{
        margin: 25% auto;
        &__img{
            max-width: 100%;
        }
    }
</style>
