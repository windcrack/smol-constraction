<template lang="pug">
    .services-block
        .claster
        h5.title {{serv.title}}
        p.services-block__descr {{serv.descr}}
        nuxt-link(to="/typicalservice").details подробней
            img(src="arrowGreen.svg").details__img
</template>

<script>
    export default {
        props:['serv']
    }
</script>

<style lang="scss">
    .services-block{
        background: #F8F8FF;
        border: 1px solid #F8F8FF;
        box-sizing: border-box;
        border-radius: 0px 30px;
        max-width: 348px;
        height: 306px;
        padding: 45px 30px 53px;
        position: relative;

        @media screen and (max-width: 1200px){
            width: 329px;
        }

        @media screen and (max-width: 600px){
            width: 285px;
            padding: 40px 0px 45px 30px;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        &:hover{
            .claster{
                opacity: 1;
            }
        }

        .title{
            color: #000;
        }

        &__descr{
            font-weight: 300;
            font-size: 16px;
            line-height: 26px;
            color: #292929;
            margin: 15px 0 20px;
        }
    }
</style>
