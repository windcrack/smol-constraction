<template lang="pug">
    .reviews
        .reviews-header
            h2.title Отзывы
            .slider__controls
                .slider__button.is-prev(ref='prev')
                    img(src="img/prev.svg")
                .slider__button.is-next(ref='next')
                    img(src="img/next.svg")
        .slider
            .slider__container(ref='container')
                .slider__wrapper
                    .slider__slide(v-for="(item, i) in reviewItems" :key="i")
                        ReviewsBody(:rev="item")
                .slider__pagination.slider__pagination_style-blog
</template>

<script>
import Swiper, { Pagination, Navigation } from 'swiper';
Swiper.use([Pagination, Navigation])
    export default {
        data(){
            return{
                reviewItems:[
                    {
                        avatar: '/avatar/avatar1.jpg', 
                        name: 'Сыпченко Владимир Евгеньевич', 
                        descr: 'В районе хорошо развита социальная и транспортная инфраструктура. В пешей доступности находятся детские сады, школы, поликлиники, магазины и фитнес-клубы. Рядом расположены живописные зелёные зоны — Волжский бульвар, обширный Кузьминский лесопарк, пруд Садки, а также музей-усадьба Кусково. Поблизости — ТЦ «Город», «Леруа Мерлен», кинотеатр «Олимпик Синема» и стадион «Москвич».', 
                        date: '12 марта 2020'
                    },
                    {
                        avatar: '/avatar/avatar2.jpg', 
                        name: 'Петров Максим Сергеевич', 
                        descr: 'В районе хорошо развита социальная и транспортная инфраструктура. В пешей доступности находятся детские сады, школы, поликлиники, магазины и фитнес-клубы. Рядом расположены живописные зелёные зоны — Волжский бульвар, обширный Кузьминский лесопарк, пруд Садки, а также музей-усадьба Кусково. Поблизости — ТЦ «Город», «Леруа Мерлен», кинотеатр «Олимпик Синема» и стадион «Москвич».', 
                        date: '12 марта 2020'
                    },
                    {
                        avatar: '/avatar/avatar1.jpg', 
                        name: 'Сыпченко Владимир Евгеньевич', 
                        descr: 'В районе хорошо развита социальная и транспортная инфраструктура. В пешей доступности находятся детские сады, школы, поликлиники, магазины и фитнес-клубы. Рядом расположены живописные зелёные зоны — Волжский бульвар, обширный Кузьминский лесопарк, пруд Садки, а также музей-усадьба Кусково. Поблизости — ТЦ «Город», «Леруа Мерлен», кинотеатр «Олимпик Синема» и стадион «Москвич».', 
                        date: '12 марта 2020'
                    },
                ]
            }
        },
        mounted(){
            setTimeout(() => {
                new Swiper(this.$refs.container, {
                        wrapperClass: 'slider__wrapper',
                        slideClass: 'slider__slide',
                        spaceBetween: 32,
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
                            1200:{
                                slidesPerView: 2,
                            },
                            768: {
                                slidesPerView: 1,
                            }
                        }
                    })
            }, 300)
        }
    }
</script>

<style lang="scss">
    .reviews{
        margin: 30px 0 34px;
        position: relative;
        overflow: hidden;

        &-header{
            position: relative;
        }

        .slider{
            margin-top: 42px;

            &__controls{
                top: 0;
                right: 0;
                left: 86%;
                bottom: 0;

                @media screen and (max-width: 1200px){
                    left: 75%;
                }

                @media screen and (max-width: 600px){
                    left: 56%;
                }
            }
        }
    }
</style>