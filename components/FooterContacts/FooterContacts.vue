<template lang="pug">
    .footer-contacts
        .social.social_end.social_mobile-start
            a(href="https://www.viber.com/ru/").socia__link
                img(src="/viber.png").social-img.social-img_left.social-img_mobile-right
            a(href="https://www.whatsapp.com/?lang=ru").socia__link
                img(src="/wtp.png").social-img.social-img_left.social-img_mobile-right
            a(href="https://web.telegram.org/#/login").socia__link
                img(src="/telegramm.png").social-img.social-img_left.social-img_mobile-right
        .phone
            a(href="tel:78885553535").phone__link +7 888 555 35 35
        .email
            a(href="mailto:smolconstruction@mail.ru").email__link smolconstruction@mail.ru
</template>

<script>
    export default {

    }
</script>

<style lang="scss">
    .social{
        @media screen and (max-width: 600px){
            justify-content: flex-start;
            margin-bottom: 35px;
        }
    }

    .phone, .email{
        text-align: right;

        @media screen and (max-width: 1200px){
            text-align: left;
        }

        &__link{
            color: #fff;
            font-weight: normal;
            font-size: 16px;
            line-height: 24px;
            text-transform: uppercase;

            @media screen and (max-width: 600px){
                font-size: 14px;
            }
        }
    }

    .phone{
        margin-bottom: 16px;
    }
</style>
