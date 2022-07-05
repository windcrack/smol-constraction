<template lang="pug">
    .popup
        .popup-body
            .popup-header
                h2.title Связаться с нами
                img(src="/close.svg" @click="close").popup-header__close
            PopupProjectService(@hideClick="close")
            PopupForm
            PopupFooter
</template>

<script>
    export default {
        props: ['visible'],

        methods:{
            close(){
                this.$modal.hide('popup')
            }
        }
    }
</script>

<style lang="scss">
    .popup{
        background: rgba(0, 0, 0, 0.35);
        display: flex;
        position: absolute;
        width: 100%;
        z-index: 100000;

        .title{
            margin-bottom: 35px;

            @media (min-width: 1200px) and (max-width: 1500px){
                margin-bottom: 0px;
            }
        }

        &-body{
            width: 484px;
            margin-left: auto;
            background: #FFFFFF;
            padding: 66px 55px 53px 77px;
            display: flex;
            flex-direction: column;
            row-gap: 2rem;

            @media (min-width: 1200px) and (max-width: 1500px){
                padding: 26px 55px 53px 77px;
                row-gap: 1rem;
            }

            @media (max-width: 1200px){
                margin-right: 0px;
                row-gap: 3rem;
            }
        }

        &-header{
            display: flex;
            justify-content: space-between;

            &__close{
                width: 10px;
                height: 10px;
                cursor: pointer;
                margin-top: 16px;
                margin-right: 27px;
            }
        }
    }
</style>
