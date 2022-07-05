<template lang="pug">
    .allKinds
        .header-title
            h1.title Все виды строительных работ
            p.sub-title.sub-title_margin44 Строительство всех видов недвижимости по  индивидульному проекту
            button.button.button_color.button_width200.button_radius30.button_border-green.button_mobile-auto.button_none-mobile
                span.button__text Подробней
        .slider-block.slider-block_mob-transform
            .slider
                .slider__container(ref='container')
                    .slider__wrapper
                        .slider__slide(v-for='(item, index) in slides', :key='index')
                            ConstractionSlide
                    .slider__controls.slider__controls_left
                        .slider__button.is-prev(ref='prev')
                            img(src="/img/prev.svg")
                        .slider__button.is-next(ref='next')
                            img(src="/img/next.svg")
                    .slider__pagination.slider__pagination_style-finishing

</template>

<script>
import Swiper, { Navigation, Pagination } from 'swiper';
Swiper.use([Navigation, Pagination])

    export default {
        data(){
            return{
                slides: [1,2],
            }
        },
        async mounted(){
            setTimeout(() => {
                new Swiper(this.$refs.container, {
                        wrapperClass: 'slider__wrapper',
                        slideClass: 'slider__slide',
                        slidesPerView: 1,
                        navigation: {
                            prevEl: this.$refs.prev,
                            nextEl: this.$refs.next,
                        },
                        pagination: {
                            el: '.slider__pagination'
                        },
                        speed: 500,
                    })
                }, 300)
        },
    }
</script>

<style lang="scss">
    .allKinds{
        color: #292929;
        display: flex;
        width: 100%;

        @media screen and (max-width: 1200px){
            flex-direction: column;
        }
    }
    

</style>