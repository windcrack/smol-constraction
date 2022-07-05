<template lang="pug">
    .project-body
        .project-wrapper
            img(:src="proj.img").project-wrapper__img
            .project-text
                h5.title {{proj.title}}
                p.sub-title {{proj.sub}}
                p.project-text__year {{proj.year}}
</template>

<script>
    export default {
        props: ['proj']
    }
</script>

<style lang="scss">
    .project-body{
        margin-bottom: 12px;
        
        @media screen and (max-width: 1200px){
            width: 329px;
        }

        @media screen and (max-width: 600px){
            width: 287px;
        }
        
        .title{
            color: #000;
        }

        .project-wrapper{
            position: relative;
            border-radius: 0 30px;

            &__img{
                border-radius: 0 30px;

                @media (max-width: 600px){
                    max-width: 100%;
                }
            }
        }

        .project-text{
            position: absolute;
            bottom: 0;
            left: 0;
            width: 271px;
            padding: 30px 24px 30px 30px;
            background: #F8F8FF;
            border-radius: 0 30px;

            display: flex;
            flex-wrap: wrap;

            &__year{
                opacity: 0.5;
                margin-left: 15px;
                position: relative;
                top: -2rem;
                bottom: 100%;

                @media (max-width: 600px){
                    margin-left: 0px;
                    top: 0rem;
                    grid-area: year;
                }
            }

            @media (max-width: 600px){
                width: 250px;
                padding: 20px 25px 18px;
                display: grid;
                grid-template-areas: "title year" "sub-title year";
            }
        }
    }
</style>