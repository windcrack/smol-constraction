<template lang="pug">
    .blog-body
        .blog-body-header
            h5.title.title_width352
                nuxt-link(to="/blogpost").blog-body-header__link {{info.title}}
                p.sub-title.sub-title_width329.sub-title {{info.descr | trimText(info.descr)}}
                    nuxt-link(to="/blogpost").green [...]
        .blog-body-footer
            .blog-body-footer__date {{info.date}}
            .blog-body-footer__button Строительство
</template>

<script>
    export default {
        props:['info'],
        filters:{
            trimText(someText){
               return someText.slice(0, 130)
            }
        }
    }
</script>

<style lang="scss">
    .blog-body{
        margin-bottom: 37px;
        display: flex;
        width: 352px;
        flex-direction: column;

        @media screen and (max-width: 600px){
            width: 285px;
        }


        &-header{
            margin-bottom: 31px;

            &__link{
                color: #22917B;
            }

            &-text{
                display: flex;
            }
        }

        &-footer{
            display: flex;
            align-items: center;

            &__button{
                width: 130px;
                padding: 8px 4px 5px 4px;
                font-weight: normal;
                font-size: 14px;
                line-height: 30px;
                text-align: center;
                color: #22917B;
                background: #F7F7FF;
                border-radius: 0px 8px;
                border: none;
                text-transform: none;

                @media screen and (max-width: 600px){
                    font-size: 12px;
                    margin-right: 20px;
                }
            }

            &__date{
                font-weight: normal;
                font-size: 14px;
                line-height: 30px;
                color: #979797;
                margin-right: 24px;

                @media screen and (max-width: 600px){
                    font-size: 12px;
                }
            }
        }
    }
</style>
