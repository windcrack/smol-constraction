<template lang="pug">
section
  .container.container_full
  .container.container_full
    AllKinds
  .container.container_full
    CompanyServices
  .container.container_no-right
    AboutCompany
  .container.container_full
    Blog
    Reviews
  .container.container_no-right
    Application
</template>

<script>
export default {
  layout: "second",
};
</script>

<style lang="scss">
.container {
  &:nth-child(2) {
    padding-right: 0 !important;

    @media screen and (max-width: 600px) {
      padding-right: 17px !important;
    }
  }
}
</style>