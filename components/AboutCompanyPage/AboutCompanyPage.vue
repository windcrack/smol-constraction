<template lang="pug">
    .about-company-head.about-company-head_mans-img
        h1.title О компании
        CompanyExperienceHead
        ul.history-list
            li.history-list__item Группа «Эталон», основанная в 1987 г. Вячеславом Заренковым, сегодня является одной из крупнейших корпораций в сфере девелопмента и строительства в России. 
            li.history-list__item За время своей работы Компания ввела в эксплуатацию более 6 миллионов квадратных метров недвижимости.
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss">
    .about-company-head{
        
        padding: 60px 0 80px;
        position: relative;

        @media screen and (max-width: 1200px){
            display: flex;
            flex-direction: column;
        }

        &_mans-img{
            background: url('/img/mans.png') no-repeat;
            background-position: 35rem 100%;

            @media screen and (max-width: 1200px){
                background-position: 1rem 100%;
                padding-bottom: 26rem;
            }

            @media screen and (max-width: 600px){
                padding-bottom: 12rem;
                background-size: 165%;
            }
        }

        &__experience{
            display: flex;
            margin-top: 39px;

            @media screen and (max-width: 600px){
                flex-direction: column;
            }

            &-item{
                width: 306px;
                height: 128px;
                box-sizing: border-box;
                border-radius: 0px 30px;
                padding: 20px 15px 28px 41px;
                display: flex;
                margin-right: 21px;

                @media screen and (max-width: 600px){
                    width: 232px;
                    margin-bottom: 20px;
                    padding: 20px 14px;
                }


                &:nth-child(2){
                    flex-direction: column;
                }

                &-years, &-happy{
                    font-weight: bold;
                    line-height: 80px;
                    letter-spacing: -0.05em;
                    text-transform: uppercase;
                    color: #239B79;
                }

                &-years{
                    font-size: 80px;
                    margin-right: 12px;
                }
                &-happy{
                    font-size: 48px;
                    &:before{
                        content:">"
                    }
                }

                &-market, &-project{
                    font-weight: normal;
                    font-size: 16px;
                    line-height: 24px;
                    color: #333;
                }

                &-market{
                    margin: auto 0;
                }

                &-project{
                    transform: translate(0, -1rem);
                }
            }
        }

        &__historyList{
            max-width: 529px;
            font-weight: normal;
            font-size: 18px;
            line-height: 27px;
            margin-top: 40px;
            margin-bottom: 8px;

            li{
                margin-bottom: 20px;
                &::marker{
                    color: #239B79;
                }
            }
        }

        &__img{
            position: absolute;
            top: 8.25rem;
            right: -29.3rem;
            bottom: 0;

            @media screen and (max-width: 1200px){
                position: relative;
                top: 0;
                right: -15rem;
            }

            @media screen and (max-width: 600px){
                right: -1rem;
                max-width: 420px !important;
                
            }
        }
        // &_mans-img{
        //     background: url('/img/mans.png') no-repeat;
        //     background-position: 35rem 100%;
        // }
    }
</style>