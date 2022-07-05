<template lang="pug">   
    .partner-list
        h3.title Партнеры
        .partner-container
            img(:src="item.url" :alt="item.alt" :title="item.alt" v-for="(item, i) in partnertsItems" :key="i").partner-container__img
</template>

<script>
    export default {
        data(){
            return{
                partnertsItems:[
                    {
                        url: '/partners/newBrand1.svg',
                        alt: 'test'
                    },
                    {
                        url: '/partners/newBrand1.svg',
                        alt: 'test'
                    },
                    {
                        url: '/partners/newBrand1.svg',
                        alt: 'test'
                    },
                    {
                        url: '/partners/newBrand1.svg',
                        alt: 'test'
                    },
                    {
                        url: '/partners/newBrand1.svg',
                        alt: 'test'
                    },
                    {
                        url: '/partners/newBrand1.svg',
                        alt: 'test'
                    },
                ],
            }
        }
    }
</script>

<style lang="scss">
    .partner-list{
        .title{
            margin-bottom: 40px;
        }
    }

    .partner-container{
        display: flex;

        @media screen and (max-width: 1200px){
            // flex-direction: column;
            flex-wrap: wrap;
        }

        &__img{
            margin-right: 80px;
            filter: grayscale(1);
            transition: all .5s;

            &:hover{
                filter: grayscale(0);
            }

            @media screen and (max-width: 1200px){
                margin-bottom: 40px;
            }

            @media screen and (max-width: 600px){
                margin-right: 40px;
                margin-bottom: 60px;
            }
        }
    }

</style>