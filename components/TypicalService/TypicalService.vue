<template lang="pug">
    .typical-header 
        .typical-header-left
            h1.title Строительство жилой недвижимости
            .details подробней
                img(src="/arrowLong.svg").details__img
        .typical-header-right
            img(src="/img/homeInTyp.png").mask.mask_for-type-mask.typical-header-right__img
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss">
    .typical-header{
        display: flex;

        @media screen and (max-width: 1200px){
            flex-direction: column;
        }

        &-left{
            margin-top: 110px;
            margin-bottom: 73px;

            @media screen and (max-width: 600px){
                margin-top: 77px;
                margin-bottom: 42px;

            }
        }

        .title{
            max-width: 541px;
            margin-bottom: 40px;

            @media screen and (max-width: 600px){
                max-width: 283px;
                margin-bottom: 35px;
            }
        }

        &-right{
            display: flex;
            align-items: flex-end;
            
            &__img{
                margin-top: auto;
                margin-left: 1rem;

                @media screen and (max-width: 600px){
                    margin: 0;
                    object-fit: contain;
                    height: 192px;
                }
            }

            @media screen and (max-width: 600px){
                height: 192px;
            }
        }

    }
</style>