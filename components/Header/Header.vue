<template lang="pug">
header#up.header
  .container-header
    nuxt-link.header-logo(to="/")
      img.header-logo__img(src="/logoHeader.svg")
    HeaderList
    button.button.button_radius30.button_hover-link.button_no-color.button_width268.button_border-green(@click="close")
      nuxt-link.button__text.button__text_green(to="#popup") связаться с нами
    .header-burger
      input#burgerBox.header-burger__input(type="checkbox")
      label.header-burger__btn(for="burgerBox", v-click-outside="hideM", @click="closeMob")
        span
    HeaderMobileList(
      v-show="mobVisible",
      :mobVisible="mobVisible",
      @hide="hideM",
      @hideClick="hideM"
    )
      nuxt-link(to="/contacts") Контакты
</template>

<script>
import ClickOutside from "vue-click-outside";

export default {
  props: ["close"],

  data() {
    return {
      mobVisible: false,
    };
  },

  methods: {
    closeMob() {
      this.mobVisible = !this.mobVisible;
    },
    hideM() {
      this.mobVisible = false;
    },
  },

  mounted() {
    this.popupItem = this.$el;
  },

  directives: {
    ClickOutside,
  },
};
</script>

<style lang="scss">
.header {
  box-shadow: 0px 4px 20px rgba(0, 0, 0, 0.05);
  padding: 22px 0;
  position: relative;

  .container-header {
    flex-direction: row;
    margin: 0 auto;
    align-items: center;
    justify-content: space-between;
    background-color: transparent;

    @media screen and (max-width: 1200px) {
      justify-content: auto;
    }

    @media screen and (max-width: 600px) {
      justify-content: space-between;
    }
  }

  &-burger {
    display: none;

    @media screen and(max-width: 1200px) {
      display: block;
      margin-right: 39px;
      width: 30px;
      height: 30px;
      padding: 5px;
    }

    @media screen and (max-width: 600px) {
      margin-right: 17px;
    }

    &__input {
      display: none;
    }

    &__btn {
      display: flex;
      align-items: center;
      width: 20px;
      height: 20px;
      position: relative;
      cursor: pointer;
      z-index: 1;
      span,
      span::after,
      span::before {
        display: block;
        position: absolute;
        width: 100%;
        height: 3px;
        background-color: #22917b;
      }

      span::before {
        content: "";
        top: -8px;
      }

      span::after {
        content: "";
        top: 8px;
      }
    }
  }

  &-logo {
    margin-left: 165px;
    @media screen and (max-width: 1200px) {
      margin-left: 39px;
      margin-right: 5rem;
    }

    @media screen and(max-width: 600px) {
      margin-left: 17px;
      // min-width: 202px;
      margin-right: 65px;
      &__img {
        max-width: 100%;
      }
    }
  }

  &-items {
    display: flex;
    list-style: none;
    padding: 0;
    margin: 0;
    position: relative;
  }

  &-item {
    margin-right: 35px;
    cursor: pointer;
    display: flex;
    align-items: center;
    

    &__img {
      display: flex;
      align-items: center;
      margin-left: 6px;
      width: 8px;
      height: 5px;

      &_active{
        #arrow{
          path{
            fill: #22917B;
          }
        }
      }
    }
  }

  .button {
    margin-right: 150px;
    transition: all 0.5s;

    @media screen and(max-width: 1200px) {
      margin-right: 30px;
    }

    @media screen and (max-width: 600px) {
      display: none;
    }
  }

  .active-item {
    font-weight: bold;
    font-size: 16px;
    line-height: 18px;
    color: #22917b;
  }
}
</style>
