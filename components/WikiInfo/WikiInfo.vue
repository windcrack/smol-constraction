<template lang="pug">
.wiki-info
  h1.title Вики. Информация <br> о строительстве
  .wiki-container
    WikiInfoLists
    WikiInfoText
</template>

<script>
export default {
  layout: "second",
};
</script>

<style lang="scss">
.wiki-info {
  margin-top: 91px;
  .wiki-container {
    display: flex;
    margin-top: 62px;

    @media screen and (max-width: 1200px) {
      flex-direction: column;
    }
  }
}
</style>