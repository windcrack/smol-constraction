<template lang="pug">
    .wiki-lists
        .claster
        .wiki-lists-first
            h6.title Строительство и ремонт
            ul.wiki-info-items
                li.wiki-info-item(v-for="(item, i) in categoryLists" :key="i")
                    nuxt-link(:to.prevent="item.url").wiki-info-item__link {{item.title}}
        .wiki-lists-second
            h6.title Стройматериалы
            ul.wiki-info-items
                li.wiki-info-item(v-for="(item, i) in materials" :key="i")
                    nuxt-link(:to.prevent="item.url").wiki-info-lists__link {{item.title}}
</template>

<script>
    export default {
        data(){
            return{
                categoryLists: [
                    {title: 'Дом из кирпича', url: `/wikiinfo/1`},
                    {title: 'Каркасная технология', url: `/wikiinfo/2`},
                    {title: 'Клееный брус', url: `/wikiinfo/3`},
                    {title: 'Фундамент', url: '/wikiinfo/4'},
                    {title: 'Кровля', url: `/wikiinfo/5` },
                    {title: 'Выбор отопления', url: `/wikiinfo/6` },
                    {title: 'Отделка фасада', url: `/wikiinfo/7` },
                ],
                materials:[
                    {title: 'Цемент', url: `/wikiinfo/8`},
                    {title: 'Бетон', url: `/wikiinfo/9`},
                    {title: 'Песок', url: `/wikiinfo/10`},
                    {title: 'Гипсокартон', url: `/wikiinfo/11`},
                    {title: 'Стекловата', url: `/wikiinfo/12`},
                    {title: 'Профили', url: `/wikiinfo/13`},
                    {title: 'Арматура', url: `/wikiinfo/14`},
                ]
            }
        }
    }
</script>

<style lang="scss">
    .wiki-lists{
        width: 277px;
        max-height: 696px;
        box-shadow: 0px 4px 20px rgba(8, 65, 54, 0.05);
        border-radius: 2px;
        padding: 60px 31px;
        position: relative;

        @media (max-width: 1200px){
            display: flex;
            width: 691px;
            max-height: 395px;
            margin-bottom: 68px;
        }

        @media (max-width: 600px){
            width: 100%;
            flex-direction: column;
            max-height: 100%;
            margin-bottom: 50px;
            padding-bottom: 50px;
        }

        &-first{
            @media (max-width: 1200px){
                margin-right: 112px;
            }

            @media (max-width: 600px){
                margin-right: 0px;
            }
        }

        .claster{
            width: 100px;
            right: 2rem;
        }

        .title{
            margin-bottom: 14px;
        }
    }

    .wiki-info{
        &-items{
            list-style: none;
            padding-left: 0;
            margin-left: 0;
            font-weight: 300;
            font-size: 16px;
            line-height: 26px;
            color: #2B3436;
            margin-bottom: 30px;
        }

        &-item{
            padding-bottom: 8px;
            font-weight: 300;
            font-size: 16px;
            line-height: 26px;
            color: #2B3436;
            &__link{
                font-weight: 300;
                font-size: 16px;
                line-height: 26px;
                color: #2B3436;
            }
        }

        .nuxt-link-active{
            font-weight: 500;
            color: #22917B;
            display: flex;
            align-content: center;
            &:before{
                content: url('../../static/listGreen.svg');
                margin-right: 10px;
                transform: translateY(-3px);
            }
        }
    }
</style>
