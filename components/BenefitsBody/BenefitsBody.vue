<template lang="pug">
    .benefits-body
        .benefits-circle
            img(:src="bene.img").benefits-circle__img
        .benefits-text
            h4.title {{bene.title}}
            p.sub-title {{bene.subTitle}}
</template>

<script>
    export default {
        props:['bene']
    }
</script>

<style lang="scss">
    .benefits-body{
        width: 495px;
        display: flex;
        align-items: center;
        margin-bottom: 60px;

        @media screen and (max-width: 1200px){
            margin-bottom: 40px;
        }

        @media screen and (max-width: 600px){
            width: 285px;
            align-items: flex-start;

        }

        .title{
            margin-bottom: 15px;
        }
    }
    
    .benefits-circle{
        background: #F8F8FF;
        border-radius: 50%;
        min-width: 120px;
        height: 120px;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 32px 26px;

        @media (max-width: 600px){
            min-width: 60px;
            height: 60px;
            padding: 16px 13px;
        }

        &__img{
            @media (max-width: 600px){
                max-width: 100%;
            }
        }
    }

    .benefits-text{
        margin-left: 40px;
        
        @media screen and (max-width: 600px){
            margin-left: 20px;
        }
    }
        
</style>