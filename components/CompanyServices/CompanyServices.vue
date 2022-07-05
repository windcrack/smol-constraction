<template lang="pug">
.company-services
    h2.title Услуги компании
    .slider-block.slider-block_marging-top
      .slider
        .slider__container(ref="container")
            .slider__wrapper
                .slider__slide(v-for="(item, i) in serviceItems", :key="i")
                    CompanyServicesBody(:serv="item")
            .slider__pagination.slider__pagination_style-blog.slider__pagination_small-margin.slider__pagination_no-block
</template>

<script>
import Swiper, { Pagination } from "swiper";
Swiper.use([Pagination]);
export default {
  data() {
    return {
      serviceItems: [
            {
                img: "img/home.svg",
                title: "Строительство всех видов, недвижимости",
            },
            {
                img: "img/create.svg",
                title: "Создание технического проект",
            },
            {
                img: "img/disigne.svg",
                title: "Создание дизайн проекта",
            },
        
        ],
    };
  },
  mounted() {
    setTimeout(() => {
      new Swiper(this.$refs.container, {
        wrapperClass: "slider__wrapper",
        slideClass: "slider__slide",
        spaceBetween: 28,
        speed: 500,
        pagination: {
          el: ".slider__pagination",
        },
        breakpoints: {
          1200: {
            slidesPerView: 3,
          },

          768: {
            slidesPerView: 2,
          },
          320: {
            slidesPerView: 1,
          },
        },
      });
    }, 300);
  },
};
</script>

<style lang="scss">
    .company-services{
        margin: 80px 0 103px;
    }
    .slider-block{

        &__items{
            margin-top: 43px;
        }

        &__wrapper{
            display: flex;
        }

        &__paginations{
            display: none;
            
            @media screen and (max-width: 1200px){
                display: flex;
                justify-content: center;
                align-items: center;
            }

            .swiper-pagination-bullet{
                display: flex;
                border-radius: 50%;
                margin-right: 12px;
                background: #22917B;
                opacity: 0.5;
                width: 8px;
                height: 8px;
                &-active{
                    opacity: 1;
                }
            }
        }
    }
</style>