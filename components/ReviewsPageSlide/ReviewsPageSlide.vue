<template lang="pug">
    .reviews-page-slider
        .reviews-page-slider__img(ref="slider")
            .shadow
                img(src="/img/plus.png" @click="show").shadow__img
            img(:src="slide")
</template>

<script>
import ReviewsModal from '../ReviewsModal/ReviewsModal'
    export default {
        props:['slide'],
        data(){
            return{
                width: 0,
            }
        },
        mounted(){
            this.width = this.$refs.slider.offsetWidth;
            console.log(this.width);
        },
        methods:{
            show(){
                this.$modal.show(ReviewsModal,
                    {
                        slides:{
                            slide: this.slide
                        }
                    },
                    {
                        reset: true,
                        adaptive: true,
                        height: 'auto',
                        scrollable: true,

                    },
                    {
                        text: 'test'
                    },
                )
            },
        }

    }
</script>

<style lang="scss">
    .reviews-page-slider{
        img{
            @media screen and (max-width: 600px){
                max-width: none !important;
            }
        }
        .shadow{
            display: none;
        }

        &:hover{
            .shadow{
                display: flex;
            }
        }

        &__img{
            position: relative;
        }
    }
</style>
