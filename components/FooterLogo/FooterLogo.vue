<template lang="pug">
    .footer-logo
        img(src="/logoWhite.svg").logo-img
        .sub-link
            nuxt-link(to="/privacypolicy").sub-link__privacy.sub-link__privacy_line Политика конфиденциальности
            a(href="https://dancecolor.ru/").sub-link__dancecolor Сделано в Dancecolor
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss">
    .footer-logo{
        display: flex;
        flex-wrap: wrap;
        max-width: 371px;

        @media screen and (max-width: 1200px){
            margin-bottom: 45px;
        }
    }

    .logo-img{
        margin-bottom: 34px;

        @media screen and (max-width: 1200px){
            margin-bottom: 45px;
        }

        @media screen and (max-width: 600px){
            flex-direction: column;
            flex-wrap: nowrap;
        }
    }
        
    .sub-link{

        @media screen and (max-width: 600px){
            display: flex;
            flex-direction: column;
        }

        &__privacy, &__dancecolor{
            flex-basis: 50%;
            font-weight: normal;
            font-size: 12px;
            line-height: 32px;
            letter-spacing: 0.05em;
            color: #FFFFFF;
            opacity: 0.5;
            text-wrap: nowrap;
        }

        &__privacy{
            margin-right: 36px;
            &_line{
                text-decoration: underline;

                @media screen and (max-width: 600px){
                    margin-left: 0;
                }
            }
        }
    }
</style>