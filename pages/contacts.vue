<template lang="pug">
section
  .container.container_full
    BreadCrums
    Contacts
  .container.container_no-right
    Application
</template>

<script>
export default {
    layout: "second",
    // async asyncData({$axios}){
    //     const db = await $axios.$get('app.json')
    //     return {db}
    // }
};
</script>

<style lang="scss">
</style>
