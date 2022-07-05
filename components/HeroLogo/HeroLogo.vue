<template lang="pug">
    .hero-logo
        img(src="logoMain.svg").hero-logo__img
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss">
    .hero-logo{
        display: flex;
        width: 100%;
        margin: 60px auto 108px;

        @media (max-width: 1200px){
            width: 250px;
            height: 35px;
            margin: 35px auto 40px;
        }

        &__img{
            margin: 0 auto;
            @media (max-width: 1200px){
                width: 100%;
            }
        }
      }
</style>