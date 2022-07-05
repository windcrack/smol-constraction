<template lang="pug">
    .popup-footer
        .popup-footer-block
            img(src="/mailPopup.svg").popup-footer__img
            a(href="mailto:smolconstruction@mail.ru").popup-footer__link smolconstruction@mail.ru
        .popup-footer-block
            img(src="/phonePopup.svg").popup-footer__img
            a(href="tel:+7 888 555 35 35").popup-footer__link +7 888 555 35 35
        .popup-footer-block
            img(src="/instPopup.svg").popup-footer__img
            a(href="instagram.com").popup-footer__link Подписывайтесь
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss">
    .popup-footer{
        &-block{
            display: flex;
            align-items: center;
            margin-bottom: 16px;
        }

        &__img{
            margin-right: 24px;
        }
    }
</style>