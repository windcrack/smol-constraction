<template lang="pug">
    .hero-footer
        a(href="mailto:test@mail.ru").footer-link
            img(src="/img/mail.svg").footer-link__img
            span.footer-link__text smolconstruction@mail.ru
        a(href="tel:78885553535").footer-link
            img(src="/img/phone.svg").footer-link__img
            span.footer-link__text +7 888 555 35 35
        a(href="https://www.instagram.com/").footer-link
            img(src="/img/instagram.svg").footer-link__img
            span.footer-link__text Подписывайтесь
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss">
    .hero-footer{
        margin: 0 auto 60px;
        display: flex;
        justify-content: space-around;
        width: 70%;
        background: transparent;

        @media screen and (max-width: 1200px){
            width: 100%;
        }

        @media screen and (max-width: 600px){
            flex-direction: column;
            margin-bottom: 35px;
        }
    }
    .footer-link{
        display: flex;
        align-items: center;
        text-decoration: none;
        color: #333;
        font-style: normal;
        font-weight: 500;
        font-size: 22px;
        line-height: 27px;

        @media screen and (max-width: 1200px){
            font-size: 18px;
        }
        
        &__img{
            margin-right: 18px;
        }
    }
</style>