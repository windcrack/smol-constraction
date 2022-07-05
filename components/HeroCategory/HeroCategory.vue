<template lang="pug">
    .hero-category
        .finishing
            h2.hero-title Все виды отделочных работ
            nuxt-link(to="/finishing").button.button_no-color.button_radius20.button_border-white.button_width168.button_margin.button_mobile-style-hero
                a.button__text.button__text_mobile-text Подробней
            img(src="/img/finishing.png").finishing__img
        .construction
            h2.hero-title Все виды строительных услуг
            nuxt-link(to="/construction").button.button_no-color.button_radius20.button_border-white.button_width168.button_margin.button_mobile-style-hero
                a.button__text.button__text_mobile-text Подробней
            img(src="/img/construction.png").construction__img
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss">
    .hero-category{
		display: flex;
		margin: 0 auto 121px;

        @media screen and (max-width: 1200px){
            margin-bottom: 0;
        }

        @media screen and (max-width: 600px){
            margin-bottom: 28px;
            flex-direction: column;
        }
    }
    .finishing, 
    .construction{
        display: flex;
        flex-direction: column;
        width: 540px;
        height: 585px;
        background: linear-gradient(50.2deg, #22917B 12.16%, #22B573 92.67%);
        transition: all .3s;
        position: relative;

        @media screen and (max-width: 1200px){
            width: 333px;
            height: 348px;
            transition: none;
        }

        @media screen and (max-width: 600px){
            width: 285px;
            height: auto;
            overflow: hidden;
        }

        &__img{
            margin-top: auto;

            @media (max-width: 1200px){
                max-width: 100%
            }
            @media (max-width: 600px){
                max-width: 100%;
                position: absolute;
                right: -7rem;
                bottom: 0;
            }
        }

        @media screen and (min-width: 1200px){
            &:hover{
                transform: scale(1.2);
            }
        }
    }

    .hero-title{
        font-weight: bold;
        font-size: 45px;
        line-height: 47px;
        text-align: center;
        color: #FBFBFF;
        max-width: 344px;
        margin: 52px auto 45px;

        @media screen and (max-width: 1200px){
            width: 259px;
            margin: 31px auto 11px;
            font-size: 28px;
            line-height: 30px;
            text-align: center;
        }

        @media screen and (max-width: 600px){
            margin-top: 17px;
            margin-left: 21px;
            text-align: left;
            margin-bottom: 21px;
            font-size: 22px;
            line-height: 24px;
            width: 172px;
        }
    }
</style>