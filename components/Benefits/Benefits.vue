<template lang="pug">
    .benefits
        .benefits-block(v-for="item in benefitsItems" :key="item.img")
            BenefitsBody(:bene="item")
</template>

<script>
    export default {
        data(){
            return{
                benefitsItems:[
                    {
                        img: '/img/protactor1.svg',
                        title: 'Гибкий подход',
                        subTitle: 'Мы составляем индивидуальные планировки без увеличения стоимости проектирования и строительства.',
                    },
                    {
                        img: '/img/floor1.svg',
                        title: 'Качественные материалы',
                        subTitle: 'Мы используем сертифицированные материалы от крупнейших поставщиков и производителей, соответствующие ГОСТам и стандартам РФ.',
                    },
                    {
                        img: '/img/money1.svg',
                        title: 'Фиксированная цена',
                        subTitle: 'Цена фиксируется на момент заключения договора и не меняется в процессе строительства.',
                    },
                    {
                        img: '/img/architect1.svg',
                        title: 'Квалифицированные специалисты',
                        subTitle: 'Опытные прорабы, мастера и бригады, работающие в компании на постоянной основе.',
                    },
                ]
            }
        }
    }
</script>

<style lang="scss">
    .benefits{
        margin: 80px 0 120px;
        display: flex;
        flex-wrap: wrap;

        &-block{
            margin-right: 58px;
            &:nth-child(2n){
                margin-right: 0px;
            }
        }
    }
</style>