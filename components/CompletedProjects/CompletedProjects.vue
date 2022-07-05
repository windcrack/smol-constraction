<template lang="pug">
    .completed-projects
        .completed-header
            h2.title.title_mobile-width232 Выполненные проекты
            .slider__controls.slider__controls_progect
                .slider__button.is-prev(ref='prev')
                    img(src="/img/prev.svg")
                .slider__button.is-next(ref='next')
                    img(src="/img/next.svg")
        .completed-slider
            .slider
                .slider__container(ref='container')
                    .slider__wrapper
                        .slider__slide.slider__slide_slide-complete(v-for="(item, i) in projectItems" :key="i")
                            nuxt-link(to="/portfolio")
                                CompletedProjectsBody(:proj="item")
                    .slider__pagination.slider__pagination_style-blog

</template>

<script>
import Swiper, { Pagination, Navigation } from 'swiper';
Swiper.use([Pagination, Navigation]);
    export default {
        data(){
            return{
                projectItems:[
                    {
                        img: '/img/img1-1.png',
                        title: 'RiverSky',
                        sub: 'м. «Автозаводская»',
                        year: '2016 г.',
                    },
                    {
                        img: '/img/img1-2.png',
                        title: 'RiverSky',
                        sub: 'м. «Автозаводская»',
                        year: '2016 г.',
                    },
                    {
                        img: '/img/img1-3.png',
                        title: 'RiverSky',
                        sub: 'м. «Автозаводская»',
                        year: '2016 г.',
                    },
                    {
                        img: '/img/img1-1.png',
                        title: 'RiverSky',
                        sub: 'м. «Автозаводская»',
                        year: '2016 г.',
                    },
                    {
                        img: '/img/img1-2.png',
                        title: 'RiverSky',
                        sub: 'м. «Автозаводская»',
                        year: '2016 г.',
                    },
                ],
            }
        },
        mounted(){
            setTimeout(() => {
                new Swiper(this.$refs.container, {
                        wrapperClass: 'slider__wrapper',
                        slideClass: 'slider__slide',
                        spaceBetween: 30,
                        pagination:{
                            el: '.slider__pagination'
                        },
                        navigation:{
                            prevEl: this.$refs.prev,
                            nextEl: this.$refs.next,
                        },
                        speed: 500,
                        breakpoints:{
                            1200: {
                                slidesPerView: 3,
                            },
                            768:{
                                slidesPerView: 2,
                            },
                            320:{
                                slidesPerView: 1,
                                spaceBetween: 17,
                            }
                        }
                    })
            }, 300)
        }
    }
</script>

<style lang="scss">
    .completed-projects{
        margin-top: 100px;
        margin-bottom: 82px;
        overflow: hidden;
    }
    .completed-header{
        position: relative;
        display: flex;
        align-items: center;
        margin-bottom: 52px;

        @media screen and (max-width: 600px){
            align-items: flex-start;
            margin-bottom: 30px;
            flex-direction: column;
        }
    }

    .slider{

    }
</style>
