<template lang="pug">
    .vacancies-form#vacForm
        h2.title Отправить анкету
        .vacancies-block
            VacancyBodyForm
        img(src="/img/greenblock2.png").green-block.green-block_form-one
        img(src="/img/greenblock2.png").green-block.green-block_form-two
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss">
    .vacancies-form{
        max-width: 483px;
        margin: 0 auto 79px;
        position: relative;
        .title{
            margin: 65px auto 47px;
        }
    }
    .vacancies-block{
        display: flex;
        flex-direction: column;
    }
</style>