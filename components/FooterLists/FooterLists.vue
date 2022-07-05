<template lang="pug">
    .footer-lists
        .lists-first
            h6.title.title_white Услуги
            ul.lists-items
                li.lists-items__item
                    nuxt-link(to="/typicalservice") Строительство домов под ключ
                li.lists-items__item
                    nuxt-link(to="/typicalservice") Ремонтные и отделочные работы
                li.lists-items__item
                    nuxt-link(to="/typicalservice") Создание проекта под ключ
                li.lists-items__item
                    nuxt-link(to="/typicalservice") Каталог товаров
        .lists-second
            h6.title.title_white О компании
            ul.lists-items
                li.lists-items__item
                    nuxt-link(to="/about") О нас
                li.lists-items__item
                    nuxt-link(to="/portfolio") Портфолио
                li.lists-items__item
                    nuxt-link(to="/contacts") Контакты
                li.lists-items__item Доставка и оплата
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss">
    .footer-lists{
        color: #fff;
        display: flex;

        @media screen and (max-width: 600px){
            justify-content: space-between;
            flex-direction: row-reverse;
            width: 100%;
        }
    }

    .lists-first{
        margin-right: 55px;

        @media screen and (max-width: 600px){
            margin-right: 0px;
            margin-left: auto;
        }
    }
    
    .lists-second{
        @media screen and (max-width: 600px){
            // margin-right: 47px;
        }
    }

    .lists-items{
        font-weight: normal;
        list-style-type: none;
        margin-left: 0;
        padding-left: 0;
        margin-top: 20px;

        @media screen and (max-width: 600px){
            max-width: 133px;
        }

        &__item{
            padding-bottom: 15px;
            font-weight: normal;
            font-size: 12px;
            line-height: 14px;

            a{
                color: #FFFFFF;
            }

            @media screen and (max-width: 600px){
                padding-right: 22px;
            }
        }
    }
</style>