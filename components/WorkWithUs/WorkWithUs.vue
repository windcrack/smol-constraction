<template lang="pug">
    .work
        .work-left
            h2.title Работайте с нами
            p.sub-title.sub-title_top-bottom С другой стороны, укрепление и развитие внутренней структуры, а также свежий взгляд на привычные вещи - безусловно открывает новые горизонты для первоочередных требований.
            button.button.button_color.button_radius30.button_border-green.button_width229(v-scroll-to="'#vacForm'") 
                span.button__text заполнить анкету
        .work-right
            img(src="/img/manVac.png").work-right__img
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss">
    .work{
        display: flex;
        justify-content: space-between;

        @media screen and (max-width: 1200px){
            flex-direction: column;
        }

        &-left{
            padding: 95px 53px 95px 0;
        }
        &-right{
            &__img{
                @media screen and (max-width: 600px){
                    max-width: 100%;
                }
            }
        }
    }
</style>