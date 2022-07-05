<template lang="pug">
    .team-body
        .team-img
            .block-shadow
            img(:src="team.img")
        .team-info
            h6.team-info__name {{team.nameTeam}}
            p.team-info__prof {{team.prof}}
</template>

<script>
    export default {
        props:['team']
    }
</script>

<style lang="scss">
    .team-body{
        background: #F8F8FF;
        color: #333333;
        border-radius: 0px 41px;

        @media screen and (max-width: 1200px){
            width: 330px;
        }

        @media screen and (max-width: 600px){
            width: 100%;
        }

        .block-shadow{
            display: none;
            z-index: 2;
            border-radius: 0px 41px 0 0;
        }

        &:hover{
            .team-info{
                color: #fff;
                background: #22917B;
                border-radius: 0 0 0 41px;
            }

            .block-shadow{
                display: block;
            }
        }
    }
    .team-img{
        position: relative;
        z-index: 1;
        overflow: hidden;
        max-height: 239px;
        border-radius: 0 41px 0 0;

        img{
            width: 255px;
            border-radius: 0 41px 0 0;

            @media screen and (max-width: 1200px){
                width: 330px;
            }
        }
    }
    .team-info{
        padding: 25px;
        &__name{
            font-weight: 500;
            font-size: 18px;
            line-height: 24px;
            margin-bottom: 5px;
        }

        &__prof{
            font-weight: 300;
            font-size: 16px;
            line-height: 26px;
            opacity: 0.8;
        }
    }
</style>