<template lang="pug">
    .portfolio
        h1.title Портфолио
        .portfolio-wrapper
            .portfolio-container(v-for="(item, i) in portfolioItems" :key="i")
                PortfolioBody(:portf="item")
</template>

<script>
    export default {
        // props: ['portfolio'],
        data(){
            return{
                portfolioItems:[
                    { img: '/img/river.png', title:'RiverSky', subTitle: 'м. «Автозаводская»', year: '2016 г.' },
                    { img: '/img/river.png', title:'RiverSky', subTitle: 'м. «Автозаводская»', year: '2016 г.' },
                    { img: '/img/river.png', title:'RiverSky', subTitle: 'м. «Автозаводская»', year: '2016 г.' },
                    { img: '/img/river.png', title:'RiverSky', subTitle: 'м. «Автозаводская»', year: '2016 г.' },
                    { img: '/img/river.png', title:'RiverSky', subTitle: 'м. «Автозаводская»', year: '2016 г.' },
                    { img: '/img/river.png', title:'RiverSky', subTitle: 'м. «Автозаводская»', year: '2016 г.' },

                ]
            }
        },
    }
</script>

<style lang="scss">
    .portfolio{
        margin-top: 91px;

        &-wrapper{
            margin-top: 61px;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
        }

        &-container{
            width: 540px;
            margin-bottom: 38px;

            @media screen and (max-width: 1200px){
                width: 692px;
            }

            @media screen and (max-width: 600px){
                margin-right: 0;
            }
        }
    }
</style>
