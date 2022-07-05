<template lang="pug">
    .sub-menu-info
        .sub-menu-info__block(@click="$emit('hide', mobVisible)")
            ul.sub-menu-info__lists(@click="$emit('toggler', visibleInfo)")
                li.sub-menu-info__list(v-for="item in infoItems" :key="item.title")
                    nuxt-link(:to="item.link") {{item.name}}
</template>

<script>
    export default {
        props: ['visibleInfo', 'mobVisible'],
        data(){
            return{
                infoItems:[
                    {link:'/about', name: 'О компании',},
                    {link:'/partners', name: 'Партнеры',},
                    {link:'/blog', name: 'Блог',},
                    {link:'/reviews', name: 'Отзывы',},
                    {link:'/wikiinfo/1', name: 'Вики. Информация о строительстве',},
                    {link:'/privacypolicy', name: 'Политика конфиденциальности',},
                    {link:'/vacancies', name: 'Вакансии',},

                ]
            }
        },
    }
</script>

<style lang="scss">
    .sub-menu-info{
        position: absolute;
        top: 3.8rem;
        left: 6rem;
        border-top: 3px solid #22917B;
        display: flex;
        background: #FFFFFF;
        box-shadow: 0px 4px 20px rgba(0, 0, 0, 0.05);
        padding: 22px 28px;
        z-index: 100;

        @media screen and (max-width: 1200px){
            position: relative;
            top: 0;
            left: 0;
            margin-bottom: 35px;
        }

        .title{
            margin-bottom: 20px;
        }

        &__block{
            &:first-child{
                margin-right: 25px;
            }
        }

        &__lists{
            font-weight: 300;
            font-size: 16px;
            line-height: 26px;
            color: #5D5D5D;
            list-style: none;
            margin-left: 0;
            padding-left: 0;
        }
        &__list{
            cursor: pointer;
        }
    }
</style>
