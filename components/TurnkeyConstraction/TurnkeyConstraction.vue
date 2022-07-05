<template lang="pug">
    .turnkey-constraction
        .turnkey-left
            h3.title Строительство под ключ
            p.sub-title Все заботы связанные со строительством дома мы возьмем на себя: разработка проекта дома, закупки и доставки материалов, организация всех строительных процессов.
            ol.turnkey-lists
                li.sub-title.turnkey-lists__item Мы разрабатываем индивидуальный проект или вы выбирите готовый.
                li.sub-title.turnkey-lists__item Вы заключаете с нами договор.
                li.sub-title.turnkey-lists__item Через 3 – 6 месяцев вы получаете готовый дом.
            button.button.button_color.button_width229.button_border-green.button_radius30(v-scroll-to="'#appli'") 
                span.button__text оставить заявку
        .turnkey-right
            img(src="/img/homeNext.png").turnkey-right__img
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss">
    .turnkey-constraction{
        display: flex;
        flex-direction: row-reverse;
        margin: 75px 0 86px;
    }

    .turnkey-left{
        margin-left: auto;
        max-width: 540px;
        margin-top: 22px;

        @media screen and (max-width: 1200px){
            max-width: 100%;
        }
    }

    .title{
        margin-bottom: 15px;
    }

    .turnkey-lists{
        margin-top: 25px;
        margin-bottom: 50px;
        &__item{
            margin-bottom: 15px;
            &::marker{
                color: #22917B;
            }
        }

        @media screen and (max-width: 600px){
            padding-left: 1rem;
        }
    }

    .turnkey-right{
        &__img{
            border-radius: 0px 40px;

            @media screen and (max-width: 1200px){
                display: none;
            }
        }
    }
</style>