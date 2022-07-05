<template lang="pug">
    .video-body
        iframe(
                :src="url" 
                frameborder="0" 
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
                allowfullscreen
            ).video-body__iframe
</template>

<script>
    export default {
        props:['url']
    }
</script>

<style lang="scss">
    .video-body{
        &__iframe{
            width: 350px;
            height: 250px;

            @media screen and (max-width: 1200px){
                width: 327px;
                height: 260px;
            }

            @media screen and (max-width: 600px){
                width: 285px;
            }
        }
    }
</style>