<template lang="pug">
    .about-company.about-company_mans-img
        h2.title О компании
        CompanyExperience
        ul.history-list
            li.history-list__item Группа «Эталон», основанная в 1987 г. Вячеславом Заренковым, сегодня является одной из крупнейших корпораций в сфере девелопмента и строительства в России. 
            li.history-list__item За время своей работы Компания ввела в эксплуатацию более 6 миллионов квадратных метров недвижимости.
</template>

<script>

    export default {

    }
</script>

<style lang="scss">
    .about-company{
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
                background-position: 2rem 100%;
                padding-bottom: 30rem;
            }

            @media screen and (max-width: 600px){
                background-size: 165%;
                padding-bottom: 12rem;
                background-position: 1rem 100%;
            }
        }
    }

    .history-list{
        margin-left: 0;
        padding-left: 12px;
    }
</style>