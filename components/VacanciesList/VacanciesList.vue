<template lang="pug">
    .vacancies-list
        h5.title {{list.title}}
        ul.vacancies-list__items
            li.vacancies-list__item(v-for="item in list.text" :key="item") {{item}}
</template>

<script>
    export default {
        props: ['list']
    }
</script>

<style lang="scss">
    .vacancies-list{

        &__items{
            margin-bottom: 32px;
        }

        &__item{
            padding-bottom: 20px;
            &::marker{
                color: #22917B;
            }
        }
    }
</style>