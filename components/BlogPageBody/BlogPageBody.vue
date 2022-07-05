<template lang="pug">
    .blog-page-body
        h5.title.title_green.title_margin-bottom 
            nuxt-link(to="/blogpost").blog-page-body__link {{text.title}}
        p.sub-title {{text.descr}}
            nuxt-link(to="/blogpost").blog-page-body__dots [...]
        .blog-page-info
            .blog-page-info__date {{text.date}}
            .blog-page-info__category {{text.category}}
</template>

<script>
    export default {
        props:['text']
    }
</script>

<style lang="scss">
    .blog-page-info{
        display: flex;
        align-items: center;
        margin-top: 23px;

        @media screen and (max-width: 600px){
            justify-content: space-between;
        }

        &__date{
            font-weight: normal;
            font-size: 14px;
            line-height: 30px;
            color: #979797;
            margin-right: 30px;

            @media screen and (max-width: 600px){
                margin-right: 0;
            }
        }

        &__category{
            background: rgba(34, 145, 123, 0.05);
            border-radius: 0px 8px;
            padding: 4px 14px;
            font-weight: normal;
            font-size: 14px;
            line-height: 30px;
            color: #22917B;
        }
    }

    .blog-page-body{
        &__dots{
            color: #22917B;
            margin-left: 12px;
        }

        &__link{
            color: #22917B
        }
    }
    
</style>