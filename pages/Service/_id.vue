<template lang="pug">
  .container.container_full
    BreadCrums
    BlogPage
</template>

<script>
export default {
  layout: "second",
  mounted() {
    console.log(this.$route.params.id);
  },
  async fetch() {
    // this.$axios.$get(`/api/service/${this.id}`);
  },
};
</script>

<style lang="scss">
</style>