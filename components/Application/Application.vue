<template lang="pug">
    .application.application_img#appli
        .application-header
            h2.title Оставить заявку
            p.sub-title.sub-title_width250 И наш менеджер свяжется с Вами в ближайшее время.
        ApplicationForm
        //- SendApplication
</template>

<script>
    export default {
    
    }
</script>

<style lang="scss">
    .application{
        padding-top: 68px;
        padding-bottom: 78px;
        display: flex;
        position: relative;

        @media screen and (max-width: 1200px){
            flex-direction: column;
        }

        &_img{
            background: url('/img/application.png') no-repeat 52.5rem 100%;
            background-size: 87%;

            @media screen and (max-width: 1200px){
                background: url('/img/application.png') no-repeat 28.5rem 100%;
                background-size: 132%;
            }
        }
    }

    .application-header{
        width: 288px;

        @media screen and (max-width: 1200px){
            width: 100%;
            margin-bottom: 51px;
        }

        @media screen and (max-width: 600px){
            margin-bottom: 25px;
        }
    }
</style>