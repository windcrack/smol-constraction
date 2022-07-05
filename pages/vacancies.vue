<template lang="pug">
section
  .container.container_full
    Vacancies
  .container.container_full
    WorkWithUs
  .container.container_full
    Team
  .container.container_full
    VacanciesForm
</template>

<script>
export default {
  layout: "second",
};
</script>

<style lang="scss">
.container {
  &:nth-child(2) {
    padding-right: 0;
  }
}
</style>