<template lang="pug">
    .type-slider
        .slider
            .slider__container.slider__container_hiddden(ref='container')
                .slider__wrapper.slider__wrapper_width920
                    .slider__slide.slider_slide_width(v-for="(item, i) in portTypicalItems" :key="i")
                        PortfolioTypicalSlideBody(:pti="item")
                .slider__pagination.slider__pagination_style-blog
            .slider__controls.slider__controls_btn-portfolio
                .slider__button.is-prev(ref='prev')
                    img(src="/img/prev.svg")
                .slider__button.is-next(ref='next')
                    img(src="/img/next.svg")
</template>

<script>
import Swiper, { Pagination, Navigation } from 'swiper';
Swiper.use([Pagination, Navigation])
    export default {
        data(){
            return{
                portTypicalItems:[
                    '/img/typeSlide.png',
                    '/img/typeSlide.png',
                    // '/img/typeSlide.png',
                ]
            }
        },
        mounted(){
            setTimeout(() => {
                new Swiper(this.$refs.container, {
                        wrapperClass: 'slider__wrapper',
                        slideClass: 'slider__slide',
                        slidesPerView: 1,
                        spaceBetween: 10,
                        centeredSlides: true,
                        pagination:{
                            el: '.slider__pagination',
                            clickable: true,
                        },
                        navigation:{
                            prevEl: this.$refs.prev,
                            nextEl: this.$refs.next,
                        },
                        speed: 500,
                        breakpoints: {
                            768:{
                                spaceBetween: 20,
                            }
                        },
                    })
            }, 300)
        }
    }
</script>

<style lang="scss">
    .type-slider{
        position: relative;
        margin-bottom: 80px;
        margin-left: auto;
        margin-right: auto;

        .slider{
            position: relative;

            &__pagination{
                margin-top: 30px;
            }

        }
    }
</style>