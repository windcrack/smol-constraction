<template lang="pug">
    .team
        h2.title Команда
        .slider
            .slider__container(ref='container')
                .slider__wrapper.team-wrapper
                    .slider__slide(v-for="(item, i) in teamItems" :key="i")
                        TeamBody(:team="item") 
                .slider__pagination.slider__pagination_style-blog
</template>

<script>
import Swiper, { Pagination } from 'swiper';
Swiper.use([Pagination])
    export default {
        data(){
            return{
                teamItems:[
                    {img:'/team/team1.png', nameTeam: 'Сыпченко Владимир Евгеньевич', prof: 'Инженер'},
                    {img:'/team/team1.png', nameTeam: 'Сыпченко Владимир Евгеньевич', prof: 'Инженер'},
                    {img:'/team/team2.png', nameTeam: 'Сыпченко Владимир Евгеньевич', prof: 'Инженер'},
                    {img:'/team/team3.png', nameTeam: 'Сыпченко Владимир Евгеньевич', prof: 'Инженер'},
                ]
            }
        },
        mounted(){
            setTimeout(() => {
                new Swiper(this.$refs.container, {
                        wrapperClass: 'slider__wrapper',
                        slideClass: 'slider__slide',
                        spaceBetween: 30,
                        pagination: {
                            el: '.slider__pagination'
                        },
                        speed: 500,
                        breakpoints:{
                            1200: {
                                slidesPerView: 4,
                            },
                            768: {
                                slidesPerView: 2,
                            },
                        }
                    })
                }, 300)
        },
    }
</script>

<style lang="scss">
    .team{
        margin: 80px 0;

        @media screen and (max-width: 1200px){
            overflow-x: hidden;
        }
        
        &-wrapper{
            margin-top: 37px;
            display: flex;
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
    }
</style>