<template lang="pug">
    .popup-service(@click="close")
        .popup-service-block
            img(src="/img/projectPopup.png").popup-service-block__img
            nuxt-link(to="/portfolio")
                span.popup-service-block__text Проекты
        .popup-service-block
            img(src="/img/servecePopup.png").popup-service-block__img
            nuxt-link(to="/services")
                span.popup-service-block__text Услуги
</template>

<script>
    export default {
        methods:{
            close(){
                this.$modal.hide('popup')
            }
        }
    }
</script>

<style lang="scss">
    .popup-service{

        &-block{
            display: flex;
            margin-bottom: 17px;
            align-items: center;

            &__img{
                border-radius: 50%;
                margin-right: 26px;
            }
        }
    }
</style>
