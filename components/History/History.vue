<template lang="pug">
    .history
        h2.title История
        .history-wrapper
            .history-list(v-for="(item, i) in infoHistory" :key="i")
                .history__border
                HistoryBody(:text="item")
</template>

<script>
    export default {
        data(){
            return{
                infoHistory:[
                    {title: '2004 — Формирование компании', descr: 'С 2004 года Группа «Эталон» работает на рынке Санкт-Петербурга, с 2006 — на рынке Москвы.'},
                    {title: '2006 — Выход на рынок Москвы и получение кредитного рейтинга', descr: 'Группа «Эталон» первой среди всех российских строительных компаний получила кредитный рейтинг от крупнейшего и наиболее консервативного международного рейтингового агентства S&P Global Ratings.'},
                    {title: '2009 — Выход на рынок Московской области', descr: 'Компания выходит на рынок Московской области с проектом комплексного освоения территории «Изумрудные холмы».'},
                    {title: '2014 — Завершение строительства «Экспоформума»', descr: 'В Санкт-Петербурге Группа «Эталон» ввела в эксплуатацию крупнейший в Восточной Европе конгрессно-выставочный центр «ЭкспоФорум».'},

                ]
            }
        }
    }
</script>

<style lang="scss">
    .history{
        margin: 60px 0;
        &-wrapper{
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            position: relative;

            @media screen and (max-width: 1200px){
                display: flex;
                flex-direction: column;
            }
        }

        &-list{
            margin-bottom: 40px;
            margin-top: 37px;
            position: relative;
            max-width: 506px;
            @media screen and (max-width: 1200px){
               min-height: 193px;
            }
        }

        &__border{
            background: linear-gradient(50.2deg, #22917B 12.16%, #22B573 92.67%);
            width: 4px;
            height: 100%;
            position: absolute;
            top: 1px;
            left: 1px;
        }
    }
</style>