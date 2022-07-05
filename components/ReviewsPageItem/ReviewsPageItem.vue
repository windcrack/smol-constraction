<template lang="pug">
    .reviews-item
        .claster
        .reviews-item-container
            .avatar-block
                img(:src="reviews.img").avatar-block__img
                h3.avatar-block__name {{reviews.nameTitle}}
            .reviews-item-description
                .reviews-item-description__text {{reviews.text}}
                .reviews-item-description__date {{reviews.date}}
        .reviews-item-slider(v-if="reviews.ifImg")
            .slider
                .slider__container(ref='container')
                    .slider__wrapper
                        .slider__slide(v-for="(item, i) in reviews.subImg" :key="i")
                            ReviewsPageSlide(:slide="item")
                    .slider__thumbs(ref='galary')
                        .slider__thumbs-wrapper
                            .slider__thumbs-slide(v-for="item in reviews.subImg")
                                img(:src="item")
</template>

<script>
import Swiper, { Pagination, Thumbs} from 'swiper';
Swiper.use([Pagination, Thumbs])
    export default {
        props:['reviews'],
        mounted(){
            let galleryThumbs = new Swiper(this.$refs.galary, {
                wrapperClass: 'slider__thumbs-wrapper',
                slideClass: 'slider__thumbs-slide',
                slidesPerView: 2,
                spaceBetween: 20,
            });
            setTimeout(() => {
                new Swiper(this.$refs.container, {
                        wrapperClass: 'slider__wrapper',
                        slideClass: 'slider__slide',
                        slidesPerView: 1,
                        spaceBetween: 30,
                        thumbs:{
                            swiper: galleryThumbs,
                        },
                        speed: 500,
                    })
            }, 300)
        }
    }
</script>

<style lang="scss">

    .reviews-item-slider{
        width: 194px;
        padding: 0 10px;
        position: relative;
        overflow-x: hidden;
    }

    .reviews-item{
        padding: 35px 55px 45px 44px;
        background: #F8F8FF;
        border: 1px solid #F8F8FF;
        box-sizing: border-box;
        border-radius: 0px 40px;
        position: relative;
        display: flex;
        &__subImg{
            overflow-x: hidden;

            flex-basis: 20%;

            @media screen and (max-width: 1200px){
                width: 176px;
            }
        }

        @media screen and (max-width: 1200px){
            flex-direction: column;
        }

        @media screen and (max-width: 600px){
            padding: 30px 25px;
        }

        .claster{
            width: 100px;
        }

        &__header{
            display: flex;
            align-items: center;
            margin-bottom: 25px;
            grid-area: header;

            @media screen and (max-width: 600px){
                flex-direction: column;
                align-items: flex-start;
                margin-bottom: 15px;

            }
        }

        &__img{
            margin-right: 25px;

            @media screen and (max-width: 600px){
                width: 65px;
                height: 65px;
                margin-bottom: 15px;
            }
        }

        .reviews-item-description{
            max-width: 714px;
            margin-right: 85px;

            @media screen and (max-width: 600px){
                margin-right: 0px;
            }

            &__text{
                font-weight: normal;
                font-size: 16px;
                line-height: 24px;
                margin-bottom: 15px;
                color: #333333;

                @media screen and (max-width: 600px){
                    margin-right: 0px;
                }
            }

            &__date{
                font-weight: normal;
                font-size: 14px;
                line-height: 30px;
                color: #979797;
            }
        }

        &__name{
            font-weight: bold;
            font-size: 20px;
            line-height: 25px;
            color: #333333;
            max-width: 250px;
        }

        .slider{

            &__wrapper{
                margin-bottom: 20px;
            }

            &__thumbs{
                height: 100%;

                &-wrapper{
                    display: flex;
                }

                &-slide{
                    width: 42px !important;
                    height: 42px;
                }

                img{
                    width: 42px;
                    height: 42px;
                }
            }
        }
    }
</style>
