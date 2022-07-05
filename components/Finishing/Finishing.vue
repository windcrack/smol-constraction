<template lang="pug">
.finishing-section
  .header-title.header-title_width50
    h1.title Все виды отделочных работ
    p.sub-title Профессиональная отделка всех видов недвижимости
    button.button.button_color.button_width200.button_radius30.button_border-green.button_mobile-auto.button_none-mobile
      span.button__text подробнее
  .slider-block.slider-block_width65.slider-block_mob-transform
    .slider
      .slider__container(ref="container")
        .slider__wrapper
          .slider__slide(v-for="(item, index) in finishingItems", :key="index")
            FinishingSlide(:img="item")
        .slider__controls.slider__controls_left
          .slider__button.is-prev(ref="prev")
            img(src="/img/prev.svg")
          .slider__button.is-next(ref="next")
            img(src="/img/next.svg")
        .slider__pagination.slider__pagination_style-finishing
</template>

<script>
import Swiper, { Navigation, Pagination } from "swiper";
Swiper.use([Navigation, Pagination]);

export default {
  data() {
    return {
      finishingItems: [
        "img/finishSlide.png",
        "img/finishSlide.png",
      ],
    };
  },
  mounted() {
    setTimeout(() => {
      new Swiper(this.$refs.container, {
        wrapperClass: "slider__wrapper",
        slideClass: "slider__slide",
        // spaceBetween: 20,
        slidesPerView: 1,
        navigation: {
          prevEl: this.$refs.prev,
          nextEl: this.$refs.next,
        },
        pagination: {
          el: ".slider__pagination",
        },
        speed: 600,
      });
    }, 300);
  },
};
</script>

<style lang="scss">
  .finishing-section {
    display: flex;
    width: 100%;

    @media screen and (max-width: 1200px) {
      flex-direction: column;
    }

    .title {
      margin-bottom: 19px;

      @media screen and (max-width: 1200px) {
        flex-direction: column;
        text-align: center;
      }

      @media screen and (max-width: 600px) {
        width: 283px;
      }
    }

    .sub-title {
      margin-bottom: 43px;
      @media screen and (max-width: 1200px) {
        max-width: 387px;
      }

      @media screen and (max-width: 600px) {
        max-width: 270px;
      }
    }
  }

</style>