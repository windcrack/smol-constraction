<template lang="pug">
    .blog
        .blog-header
            h2.title Блог
            nuxt-link(to="/blog").button.button_radius30.button_width178px.button_hover-link.button_width178.button_border-green.button_margin-auto-left
                a.button__text.button__text_small-text все записи
        .slider
            .slider__container(ref='container')
                .slider__wrapper
                    .slider__slide(v-for="(item, i) in blogItems" :key="i")
                        BlogBody(:info="item")
                .slider__pagination.slider__pagination_style-blog
</template>

<script>
import Swiper, { Pagination } from 'swiper';
Swiper.use([Pagination])
    export default{
        data(){
            return{
                blogItems:[
                    {
                        title: 'Жилой район «Волжский парк»',
                        descr: 'В районе хорошо развита социальная и транспортная инфраструктура. В пешей доступности находятся детские сады, школы, поликлиники',
                        date: '12 декабря 2020'
                    },
                    {
                        title: 'Масштабный проект «Бутово парк 2»',
                        descr: 'В районе хорошо развита социальная и транспортная инфраструктура. В пешей доступности находятся детские сады, школы, поликлиники',
                        date: '12 декабря 2020'
                    },
                    {
                        title: 'Жилой район «Волжский парк»',
                        descr: 'В районе хорошо развита социальная и транспортная инфраструктура. В пешей доступности находятся детские сады, школы, поликлиники',
                        date: '12 декабря 2020'
                    },
                    {
                        title: 'Жилой район «Волжский парк»',
                        descr: 'В районе хорошо развита социальная и транспортная инфраструктура. В пешей доступности находятся детские сады, школы, поликлиники',
                        date: '12 декабря 2020'
                    },
                    {
                        title: 'Жилой район «Волжский парк»',
                        descr: 'В районе хорошо развита социальная и транспортная инфраструктура. В пешей доступности находятся детские сады, школы, поликлиники В районе хорошо развита социальная и транспортная инфраструктура. В пешей доступности находятся детские сады, школы, поликлиники В районе хорошо развита социальная и транспортная инфраструктура. В пешей доступности находятся детские сады, школы, поликлиники',
                        date: '12 декабря 2020'
                    },
                ]
            }
        },

        mounted(){
            setTimeout(() => {
                new Swiper(this.$refs.container, {
                        wrapperClass: 'slider__wrapper',
                        slideClass: 'slider__slide',
                        spaceBetween: 28,
                        pagination:{
                            el: '.slider__pagination',
                            clickable: true
                        },
                        speed: 500,
                        breakpoints:{
                            1200:{
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
    .blog{
        overflow: hidden;

        &-header{
            margin-top: 93px;
            margin-bottom: 42px;
            display: flex;
            justify-content: space-between;
        }
    }

</style>
