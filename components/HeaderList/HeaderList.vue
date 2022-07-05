<template lang="pug">
ul.header-items
	li.header-item(v-click-outside="hide" @click="activeId = 0" :class="activeId === 0 ? 'active-item' : ''") Услуги
		svg.header-item__img
			use(:href="activeId === 0 ? '/icons/sprite.svg#arrow-green' : '/icons/sprite.svg#arrow'")
	transition(name="show")
		HeaderSubmenuServ(v-show="activeId === 0", @toggler="hide")
	li.header-item(v-click-outside="hide" @click="activeId = 1" :class="activeId === 1 ? 'active-item' : ''") Информация
		svg.header-item__img.header-item__img_active
			use(:href="activeId === 1 ? '/icons/sprite.svg#arrow-green' : '/icons/sprite.svg#arrow'")
	transition(name="show")
		HeaderSubmenuInfo(v-show="activeId === 1", @toggler="hide")
	li.header-item(@click="hide")
		nuxt-link(to="/portfolio") Наши проекты
	li.header-item(@click="hide")
		nuxt-link(to="/contacts") Контакты
</template>

<script>
import ClickOutside from "vue-click-outside";
export default {
  data() {
    return {
      activeId: null,
    };
  },
  methods: {
    hide() {
      this.activeId = null;
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
.header-items {
  @media screen and (max-width: 1200px) {
    display: none;
  }
}

</style>
