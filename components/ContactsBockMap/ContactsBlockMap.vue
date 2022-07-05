<template lang="pug">
    .contacts-map
        .contacts-info(v-for="(item, i) of lists" :key="i")
            .label.label_white.label_weight300 {{item.label}}
            .contacts-info__text {{item.text}}
        .contacts-social
            a(href="https://vk.com/feed").contacts-social__link
                img(src="/social/vk.svg").contacts-social__img
            a(href="https://www.youtube.com/").contacts-social__link
                img(src="/social/youtube.svg").contacts-social__img
            a(href="https://www.instagram.com/").contacts-social__link
                img(src="/social/insta.svg").contacts-social__img
        nuxt-link(to="/").contacts-map__download Скачать реквизиты
</template>

<script>
    export default {
        props: ['lists']
    }
</script>

<style lang="scss">
    .contacts-map{
        width: 445px;
        height: 460px;
        background: linear-gradient(50.2deg, #22917B 12.16%, #22B573 92.67%);
        border-radius: 0px 40px;
        position: absolute;
        left: 0;
        top: 0;
        color: #fff;
        padding: 41px 54px;
        margin-bottom: 50px;

        @media screen and(max-width: 1200px){
            position: relative;
            width: 100%;
            margin-bottom: 40px;
        }

        @media screen and (max-width: 600px){
            height: 100%;
            padding: 41px 35px;

        }

        &__download{
            text-decoration: underline;
            color: #fff;
        }

    .contacts-info{
        font-weight: normal;
        font-size: 20px;
        line-height: 27px;
        list-style-type: none;
        margin-left: 0;
        padding-left: 0;

        &__text{
            margin-bottom: 20px;
        }

        @media screen and (max-width: 600px){

            font-size: 18px;
            line-height: 27px;
        }
    }

    .contacts-social{
        margin-top: 42px;
        margin-bottom: 63px;
        display: flex;
        align-items : center;

        &__img{
            margin-right: 20px;
        }
    }


    }
</style>
