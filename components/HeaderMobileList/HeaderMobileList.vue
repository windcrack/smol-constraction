<template lang="pug">
.mobile-list
  ul.mobile-list-items
    li.mobile-list-item(@click="togglevMobS", :class="{ activeClass: vMobS }") Услуги
      img.mobile-list__img(src="/arrowDownGreen.png", v-if="vMobS")
      img.mobile-list__img(src="/arrowDown.png", v-else)
    HeaderSubmenuServ(
      v-show="vMobS",
      :mobVisible="mobVisible",
      @hide="hideItems"
    )
    li.mobile-list-item(@click="togglevMobI", :class="{ activeClass: vMobI }") Информация
      img.mobile-list__img(src="/arrowDownGreen.png", v-if="vMobI")
      img.mobile-list__img(src="/arrowDown.png", v-else)
    HeaderSubmenuInfo(
      v-show="vMobI",
      :mobVisible="mobVisible",
      @hide="hideItems"
    )
    li.mobile-list-item(@click="$emit('hideClick', mobVisible)")
      nuxt-link(to="/portfolio") Наши проекты
    li.mobile-list-item(@click="$emit('hideClick', mobVisible)")
      nuxt-link(to="/contacts") Контакты
</template>

<script>
export default {
  props: ["mobVisible"],
  data() {
    return {
      vMobS: false,
      vMobI: false,
    };
  },
  methods: {
    togglevMobS() {
      this.vMobS = !this.vMobS;
      if (this.vMobI) {
        this.vMobI = false;
      }
    },
    togglevMobI() {
      this.vMobI = !this.vMobI;
      if (this.vMobS) {
        this.vMobS = false;
      }
    },
    hideItems() {
      this.vMobS = false;
      this.vMobI = false;
      this.$emit("hide", this.mobVisible);
    },
  },
};
</script>

<style lang="scss">
.mobile-list {
  position: absolute;
  width: 100%;
  background: #fff;
  box-shadow: 0px 4px 20px rgba(0, 0, 0, 0.05);
  border-radius: 0px;
  padding: 30px 40px;
  top: 6.5rem;
  left: 0;
  border-top: 4px solid #22917b;
  z-index: 10000;

  @media (max-width: 600px) {
    padding-left: 20px;
    padding-right: 20px;
    top: 4.9rem;
  }

  &-items {
    display: flex;
    list-style: none;
    padding: 0;
    margin: 0;
    position: relative;

    @media (max-width: 1200px) {
      flex-direction: column;
    }
  }

  &-item {
    margin-right: 35px;
    cursor: pointer;
    display: flex;
    align-content: center;
    position: relative;

    @media screen and (max-width: 1200px) {
      margin-bottom: 35px;
    }
  }

  &__img {
    display: flex;
    align-items: center;
    margin-left: 6px;
    margin-top: auto;
    margin-bottom: auto;
  }

  .activeClass {
    // font-weight: bold;
    font-size: 16px;
    line-height: 18px;
    color: #22917b;

    @media screen and (max-width: 1200px) {
      margin-bottom: 12px;
    }
  }
}
</style>

