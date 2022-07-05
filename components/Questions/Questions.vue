<template lang="pug">
    .questions.questions_man-block
        h2.title Часто задаваемые вопросы
        p.sub-title Если оставлись вопросы, посмотрите ответы на часто задаваемые вопросы.
        .questions-wrapper
            .questions-list(v-for="item in questionsItems" :key="item.title")
                QuestionsBody(:quest="item")
</template>

<script>
    export default {
        data(){
            return{
                questionsItems:[
                    {
                        title: 'Какой проект мне нужен, чтобы построить дом?',
                        answer: 'Проект индивидуального дома – едва ли не самый важный этап любой стройки, но эта важность часто ставится под сомнение. Многие люди готовы  переплатить и потратить больше времени во время самого строительства, но при этом сэкономить на проекте.',
                    },
                    {
                        title: 'Продаете ли вы готовые проекты?',
                        answer: 'Проект индивидуального дома – едва ли не самый важный этап любой стройки, но эта важность часто ставится под сомнение. Многие люди готовы  переплатить и потратить больше времени во время самого строительства, но при этом сэкономить на проекте.',
                    },
                    {
                        title: 'Строите ли вы дома в других городах?',
                        answer: 'Проект индивидуального дома – едва ли не самый важный этап любой стройки, но эта важность часто ставится под сомнение. Многие люди готовы  переплатить и потратить больше времени во время самого строительства, но при этом сэкономить на проекте.',
                    },
                    {
                        title: 'Сколько времени занимает строительство дома?',
                        answer: 'Проект индивидуального дома – едва ли не самый важный этап любой стройки, но эта важность часто ставится под сомнение. Многие люди готовы  переплатить и потратить больше времени во время самого строительства, но при этом сэкономить на проекте.',
                    },
                    {
                        title: 'Можно ли заказать у вас строительство поэтапно?',
                        answer: 'Проект индивидуального дома – едва ли не самый важный этап любой стройки, но эта важность часто ставится под сомнение. Многие люди готовы  переплатить и потратить больше времени во время самого строительства, но при этом сэкономить на проекте.',
                    },

                ]
            }
        }
    }
</script>

<style lang="scss">
    .questions{
        margin-top: 67px;
        padding-bottom: 81px;
        position: relative;

        &_man-block{
            background: url('/img/mainInHelm.png') 36rem 100% no-repeat;

                @media screen and (max-width: 1200px){
                    background: url('/img/mainInHelm.png') 0rem 100% no-repeat;
                }

                @media screen and (max-width: 600px){
                    background: url('/img/mainInHelm.png') 0rem 100% no-repeat;
                    background-size: 38rem;
                }
            }
        &-list{
            cursor: pointer;
        }

        @media screen and (max-width: 1200px){
            padding-bottom: 39rem;
        }

        @media screen and (max-width: 600px){
            padding-bottom: 21rem;
        }

        h2.title{
            margin-bottom: 14px;
            max-width: 540px;
        }

        .sub-title{
            margin-bottom: 20px;
            max-width: 540px;
        }
    }

</style>
