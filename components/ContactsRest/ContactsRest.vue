<template lang="pug">
    .rest
        .rest-container(v-for="(item, i) in restItems" :key="i")
            ContactsRestBlock(:res="item")
</template>

<script>
    export default {
        props: ['rest'],
        data(){
            return {
                restItems:[
                    {
                        title: 'Отдел продаж',
                        phone: '+7 888 555 35 35',
                        email: 'smolconstruction@mail.ru',
                    },
                    {
                        title: 'Технический отдел',
                        phone: '+7 888 555 35 35',
                        email: 'smolconstruction@mail.ru',
                    },
                ]
            }
        },
        mounted(){
            console.log(this.rest);
        }
    }
</script>

<style lang="scss">
    .rest{
        display: flex;
        justify-content: space-between;

        @media screen and (max-width: 1200px){
            flex-direction: column;
        }
    }
</style>
