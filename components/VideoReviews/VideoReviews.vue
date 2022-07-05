<template lang="pug">
    .video
        .video-header
            h2.title Видеообзоры
            button.button.button_no-color.button_border-green.button_radius30.button_hover-link.button_width182
                nuxt-link(to="/error").button__text.button__text_green.button__text_small-text все отзывы
        .slider
            .slider__container(ref='container')
                .slider__wrapper
                    .slider__slide(v-for="item in videoUrl" :key="item")
                        VideoReviewsBody(:url="item")
                .slider__pagination.slider__pagination_style-blog
</template>

<script>
import Swiper, { Pagination } from 'swiper';
Swiper.use([Pagination])
    export default {
        data(){
            return{
                videoUrl:[
                    'https://www.youtube-nocookie.com/embed/YJVj4XNASDk',
                    'https://www.youtube.com/embed/0ViiJ8qTCFM',
                    'https://www.youtube.com/embed/lm9olMCRCIc',
                ]
            }
        },
        mounted(){
            setTimeout(() => {
                new Swiper(this.$refs.container, {
                        wrapperClass: 'slider__wrapper',
                        slideClass: 'slider__slide',
                        spaceBetween: 29,
                        pagination:{
                            el: '.slider__pagination'
                        },
                        speed: 500,
                        breakpoints: {
                            1200: {
                                slidesPerView: 3,
                            },
                            768: {
                                slidesPerView: 2,
                            },
                            320: {
                                slidesPerView: 1,
                            }
                        }
                    })
                }, 300
            )
        },
    }
</script>

<style lang="scss">
    .video{
        margin-bottom: 85px;

        &-header{
            display: flex;
            justify-content: space-between;
            margin-bottom: 50px;
        }
        .slider{

            &__pagination{
                display: none;

                @media screen and (max-width: 1200px){
                    display: flex;
                    margin-top: 20px;
                }
            }
        }
        &__wrapper{
            display: flex;
        }
    }
</style>