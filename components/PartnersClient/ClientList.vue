<template lang="pug">
    .client-list
        h3.title Клиенты
        .client-container
            img(:src="item.url" :alt="item.alt" :title="item.alt" v-for="(item, i) of imgArray" :key="i").client-container__img
</template>

<script>
    export default {
        data(){
            return{
                imgArray:[
                    {
                        url: '/partners/newBrand2.svg',
                        alt: 'test'
                    },
                    {
                        url: '/partners/newBrand2.svg',
                        alt: 'test'
                    },
                    {
                        url: '/partners/newBrand2.svg',
                        alt: 'test'
                    },
                    {
                        url: '/partners/newBrand2.svg',
                        alt: 'test'
                    },
                    {
                        url: '/partners/newBrand2.svg',
                        alt: 'test'
                    },
                    {
                        url: '/partners/newBrand2.svg',
                        alt: 'test'
                    },
                    {
                        url: '/partners/newBrand2.svg',
                        alt: 'test'
                    },
                    {
                        url: '/partners/newBrand2.svg',
                        alt: 'test'
                    },
                    {
                        url: '/partners/newBrand2.svg',
                        alt: 'test'
                    },
                    {
                        url: '/partners/newBrand2.svg',
                        alt: 'test'
                    },
                    {
                        url: '/partners/newBrand2.svg',
                        alt: 'test'
                    },
                    {
                        url: '/partners/newBrand2.svg',
                        alt: 'test'
                    },

                ],
            }
        }
    }
</script>

<style lang="scss">
    .client-list{
        .title{
            margin-bottom: 30px;
        }
    }

    .client-container{
        // display: flex;
        // justify-content: space-between;
        // flex-wrap: wrap;
        &__img{
            margin-right: 80px;
            margin-bottom: 65px;
            filter: grayscale(1);
            transition: all .5s;

            &:hover{
                filter: grayscale(0);
            }

            @media screen and (max-width: 600px){
                margin-right: 40px;
                margin-bottom: 60px;

            }
        }
    }
</style>