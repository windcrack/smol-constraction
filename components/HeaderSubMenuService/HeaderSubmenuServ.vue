<template lang="pug">
    .sub-menu
        .sub-menu__block(v-for="item in subMenuItems" :key="item.title")
            h6.title(@click="$emit('hide', mobVisible)") {{item.title}}
                ul.sub-menu__lists(@click="$emit('toggler', visibleServ)")
                    li.sub-menu__list(v-for="item in item.lists" :key="item")
                        nuxt-link(to="/typicalservice") {{item}}
</template>

<script>
    export default {
        props: ['visibleServ', 'mobVisible'],
        data(){
            return{
                subMenuItems:[
                    {
                        title: 'Строительство',
                        lists: [
                            'Промышленной недвижимости',
                            'Коммерческой недвижимости',
                            'Жилой недвижимости'
                        ]
                    },
                    {
                        title: 'Ремонт',
                        lists: [
                            'Промышленной недвижимости',
                            'Коммерческой недвижимости',
                            'Жилой недвижимости'
                        ]
                    }
                ]
            }
        },
    }
</script>

<style lang="scss">
    .sub-menu{
        position: absolute;
        top: 3.8rem;
        left: 0;
        border-top: 3px solid #22917B;
        display: flex;
        background: #FFFFFF;
        box-shadow: 0px 4px 20px rgba(0, 0, 0, 0.05);
        padding: 28px 33px;
        z-index: 100;

        @media screen and (max-width: 1200px){
            position: relative;
            top: 0;
            left: 0;
            margin-bottom: 35px;
        }

        @media screen and (max-width: 600px){
            flex-direction: column;
        }

        .title{
            margin-bottom: 20px;
        }

        &__block{
            white-space: nowrap;
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
            margin-top: 20px;
        }
        &__list{
            cursor: pointer;
        }
    }
</style>
