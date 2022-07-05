<template lang="pug">
        .portfolio-body
            img(:src="portf.img").portfolio-img
            .portfolio-info
               h5.title.title_flex-basis {{portf.title}}
               .portfolio-info__year {{portf.year}}
               .portfolio-info__sub-title {{portf.sub}}
            nuxt-link(to="/portfoliotypical").portfolio-button
                    img(src="/img/next.svg")
</template>

<script>
    export default {
        props:['portf']
    }
</script>

<style lang="scss">
    .portfolio-body{
        position: relative;
        box-sizing: border-box;

        &:hover{
            .portfolio-button{
                display: flex;
            }
        }
    }
    .portfolio-img{
        position: relative;
        z-index: 1;
        width: 540px;

        @media screen and (max-width: 1200px){
            width: 100%;
            img{
                min-width: 100;
            }
        }
    }

    .portfolio-info{
        background: #F8F8FF;
        width: 380px;
        position: absolute;
        bottom: 3px;
        left: 0;
        z-index: 2;
        padding: 30px;
        border-radius: 0 30px 0 0;
        display: flex;
        flex-wrap: wrap;

        @media screen and (max-width: 600px){
            width: 249px;
        }

        &__year{
            flex-basis: 50%;
            padding-right: 8px;
            display: flex;
            align-items: center;
            justify-content: flex-end;
            font-weight: 300;
            font-size: 16px;
            line-height: 26px;
            color: #979797;

        }

        &__sub-title{
            margin-top: 5px;
            flex-basis: 100%;
            font-weight: 300;
            font-size: 16px;
            line-height: 26px;
            color: #292929;
        }
    }

    .portfolio-button{
        position: absolute;
        right: 0;
        bottom: 3px;
        z-index: 2;
        width: 64px;
        height: 64px;
        background: linear-gradient(50.2deg, #22917B 12.16%, #22B573 92.67%);
        display: none;
        justify-content: center;
        align-items: center;
        border-radius: 15px 0 0 0;
        cursor: pointer;

        @media screen and (max-width: 1200px){
            display: flex;
        }
    }
</style>
