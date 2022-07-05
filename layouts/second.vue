<template lang="pug">
    .second
        modal(name="popup" width="100%" height="100%")
            Popup
        Header(:close="closeCall")
        Nuxt(:db="connect")
        ArrowUp
        Footer
</template>

<script>
    export default {
        data(){
            return{
                connect: [],
                test: [],
            }
        },

        async mounted(){
            this.connect = await this.$axios.$get('app.json');
        },

        methods:{
            closeCall(){
                this.$modal.show('popup')
            },
       },
    }
</script>

<style lang="scss">
    .container{
        &:nth-child(even){
            background: #F8F8FF;
        }
    }
</style>
