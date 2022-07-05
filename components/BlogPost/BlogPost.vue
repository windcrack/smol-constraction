<template lang="pug">
    .blog-post
        h1.title Проведение капитального ремонта квартиры
        p.blog-post__date 12 марта 2020
        .blog-post-block
            img(src="/img/blogPostImg.png").blog-post-block__img
            .shadow-green
        p.sub-title Капитальный ремонт квартир ARTA позволяет создать неповторимый стиль помещения, восстановить вторичное жилье, произвести перепланировку квартиры. Ремонт включает в себя полный спектр услуг, который начинается от составления плана и заканчивается полной заменой электрики, систем коммуникации и внешнего вида помещения.
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss">
    .blog-post{
        margin-top: 91px;
        margin-bottom: 45px;

        @media screen and (max-width: 600px){
            margin-bottom: 60px;
        }
        
        .title{
            margin-bottom: 60px;
            max-width: 825px;

            @media screen and (max-width: 600px){
                margin-bottom: 50px;
            }
        }

        &__date{
            font-weight: normal;
            font-size: 14px;
            line-height: 30px;
            color: #979797;
            margin-bottom: 20px;
        }
    }
    
    .blog-post-block{
        position: relative;
        margin-bottom: 20px;

        @media screen and (max-width: 1200px){
            &__img{
                max-width: 100%;
            }
        }
    }
</style>