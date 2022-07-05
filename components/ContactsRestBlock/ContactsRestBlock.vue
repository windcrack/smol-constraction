<template lang="pug">
    .rest-block
        h5.title {{res.title}}
        .rest-text
            .rest-text-block
                label.rest-text-block__label Телефон
                nuxt-link(to="tel:78885553535").rest-text-block__link {{res.phone}}
            .rest-text-block
                label.rest-text-block__label E-mail
                nuxt-link(to="mailto:smolconstruction@mail.ru").rest-text-block__link {{res.email}}
        .rest-social
            .social.social_start
                a(href="https://www.viber.com/ru/").socia__link
                    img(src="viber.png").social-img.social-img_right
                a(href="https://www.whatsapp.com/?lang=ru").socia__link
                    img(src="wtp.png").social-img.social-img_right
                a(href="https://web.telegram.org/#/login").socia__link
                    img(src="telegramm.png").social-img.social-img_right
</template>

<script>
    export default {
        props:['res']
    }
</script>

<style lang="scss">
    .rest-block{
        background: #F8F8FF;
        width: 540px;
        padding: 35px 45px;
        border-radius: 0px 40px;

        @media screen and (max-width: 1200px){
            display: flex;
            flex-wrap: wrap;
            width: 100%;
            margin-bottom: 40px;
        }

        .title{
            color: #333;
            margin-bottom: 15px;

            @media screen and (max-width: 1200px){
                flex-basis: 100%;
            }
        }
    }

    .rest-text{
        display: flex;
        max-width: 407px;
        justify-content: space-between;
        margin-bottom: 45px;

        @media screen and (max-width: 1200px){
            // width: 100%;
            margin-right: 60px;
        }

        @media screen and (max-width: 1200px){
            max-width: 100%;
        }

        @media screen and (max-width: 600px){
            flex-direction: column;
        }

        &-block{
            display: flex;
            flex-direction: column;

            @media screen and (max-width: 1200px){
                &:first-child{
                    margin-right: 60px;
                }
            }

            &__label{
                font-weight: 300;
                font-size: 16px;
                line-height: 26px;
                color: #292929;
                opacity: 0.5;
                margin-bottom: 6px;
            }
        }
    }

        // &__phone, &__email{

        // }
</style>
