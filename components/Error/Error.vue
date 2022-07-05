<template lang="pug">
    .error
        img(src="/404.png").error__img
        h2.title Страница не найдена
        p.sub-title Возможно, страница удалена или временно недоступнка
        nuxt-link(to="/").button.button_color.button_border-green.button_radius30.button_width224.button_margin
            span.button__text на главную
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss">
    .error{
        max-width: 631px;
        margin: 152px auto 178px;
        display: flex;
        flex-direction: column;
        justify-content: center;

        @media screen and (max-width: 600px){
            max-width: 100%;
            margin: auto;
            margin: 4rem auto 8rem;

        }

        &__img{
            margin-bottom: 40px;

            @media screen and (max-width: 600px){
                max-width: 100%;
            }
        }

        .sub-title{
            text-align: center;
            margin-bottom: 70px;

            @media screen and (max-width: 600px){
                margin-bottom: 50px;
            }
        }

        .title{
            text-align: center;
            margin-bottom: 15px;
        }
    }
</style>