<template lang="pug">
    .reviews-body
        .claster
        .avatar-block
            img(:src="rev.avatar").avatar-block__img
            h3.avatar-block__name {{rev.name}}
        p.sub-title.sub-title_bottom {{rev.descr}}
        span.reviews-body-date {{rev.date}}
</template>

<script>
    export default {
        props:['rev']
    }
</script>

<style lang="scss">
    .reviews-body{
        background: #F8F8FF;
        border: 1px solid #F8F8FF;
        box-sizing: border-box;
        padding: 35px 45px 30px;
        position: relative;
        margin-bottom: 33px;
        border-radius: 0 30px;
        width: 540px;

        @media (max-width: 1200px){
            width: 690px;
        }

        @media (max-width: 600px){
            width: 284px;
            padding: 30px 25px;
        }

        .claster{
            top: 0;
            right: 3rem;

            @media (max-width: 600px){
                right: 2rem;
            }
        }

        &-date{
            font-size: 14px;
            line-height: 30px;
            color: #979797;
        }
    }
</style>
