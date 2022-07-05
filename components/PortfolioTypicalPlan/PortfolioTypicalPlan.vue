<template lang="pug">
    .plan
        .green-block.green-block_triple
            img(src="/portf.png").green-block__img.green-block__img_img50
        .green-block.green-block_four
            img(src="/portf.png").green-block__img.green-block__img_img50
        .plan-container.plan-container_img-block
            .shadow
                img(src="/img/plus.png" @click="show" ).shadow__img
            img(:src="planImg" ref="img").plan-container__img
        .plan-container.plan-container_text-block
            h4.title.title_color-white Информация о проекте
            .plan-info(v-for="(item, i) in planInfoItems" :key="i")
                p.sub-title.sub-title_color-white {{item.title}}
                p.plan-info__text {{item.text}}
</template>

<script>
import PortfolioModal from '../PortfolioModal/PortfolioModal'
    export default {
        data(){
            return{
                planInfoItems:[
                    {
                        title: 'Фундамент:',
                        text: 'Ленточный'
                    },
                    {
                        title: 'Наружные стены:',
                        text: 'Газобетон 40см + штукатурка'
                    },
                    {
                        title: 'Перекрытия:',
                        text: 'По деревянным балкам'
                    },
                    {
                        title: 'Полы:',
                        text: 'По грунту'
                    },
                    {
                        title: 'Кровля:',
                        text: 'Профлист, металлочерепица или мягкая черепица'
                    },
                    {
                        title: 'Высота потолков:',
                        text: '3 метра'
                    },

                ],
                planImg: '/img/planImg.png',
                width: 0,
            }
        },
        methods:{
            show(){
                this.$modal.show(PortfolioModal,
                    {
                        slides:{
                            slide: this.planImg
                        }
                    },
                    {
                        reset: true,
                        adaptive: true,
                        height: 'auto',
                        scrollable: true,
                    },
                    { text: 'test' },
                )
            }
        },
        mounted(){
            this.width = this.$refs.img.offsetWidth;
            console.log(this.width);
        }
    }
</script>

<style lang="scss">
    .plan{
        display: flex;
        margin-bottom: 121px;
        position: relative;

        @media screen and (max-width: 1200px){
            flex-direction: column;
        }

        @media screen and (max-width: 600px){
            margin-bottom: 80px;
        }

        .title{
            margin-bottom: 20px;
        }

        .shadow{
            border-radius: 0px 40px;
            display: none;
        }
    }

    .plan-container{
        position: relative;
        display: flex;
        justify-content: center;
        background: #F7F7F7;
        border-radius: 0px 40px;

        @media screen and (max-width: 1200px){
            margin: 0 auto 50px;
            transform: translateY(0px);
        }

        &:hover{
            .shadow{
                display: flex;
            }
        }

        &__img{
            border-radius: 0px 40px;

            @media screen and (max-width: 600px){
                max-width: 100%;
            }
        }

        &_img-block{
            max-width: 529px;
            max-height: 550px;
            transform: translateY(47px);
            align-items: center;
            margin-right: 40px;

            @media screen and (max-width: 1200px){
                transform: translateY(0);
                margin-right: auto;
                margin-top: 3rem;
            }

            @media screen and (max-width: 600px){
                width: 100%;
                height: 100%;
            }
        }

        &_text-block{
            flex-direction: column;
            background: linear-gradient(50.2deg, #22917B 12.16%, #22B573 92.67%);
            width: 503px;
            height: 560px;
            padding: 40px 31px 41px 47px;
            color: #fff;

            @media screen and (max-width: 1200px){
                margin: 0 auto 80px;
            }

            @media screen and (max-width: 600px){
                padding: 39px 22px 48px 27px;
                width: 100%;
                height: 100%;
            }
        }
    }

    .plan-info{
        margin-bottom: 20px;

        &__text{
            font-weight: normal;
            font-size: 20px;
            line-height: 27px;

            @media screen and (max-width: 600px){
                font-size: 16px;
                line-height: 27px;
            }
        }
    }
</style>
