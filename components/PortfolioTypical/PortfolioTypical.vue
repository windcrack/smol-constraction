<template lang="pug">
    .portfolio-typical-body
        h1.title Жилой комплекс Невский
        .portfolio-typical-block
            .portfolio-typical-left
                h4.title Добро пожаловать в прогрессивный бизнес-класс!
                p.sub-title.sub-title_bottom «Невский» — это мечта путешественника по жизни, который наконец обрел то, что так долго искал.  Близость метро и центра города, неповторимая архитектура и атмосферное пространство вокруг домов, собственный «Ледяной грот» и интерьер от легендарного дизайнера роскошных яхт  — главные достоинства нашего проекта. 
                p.sub-title Можно ли всегда находиться в центре динамичного мегаполиса, проживая в самом зеленом и тихом районе Москвы? Конечно, если вы выбрали "Невский"!
            .portfolio-typical-right
                img(src="/img/complecsImg.png").portfolio-typical-right__img
        p.sub-title Проект расположен вблизи лесопарка Покровское-Стрешнево и Головинских прудов, всего в 5 мин. ходьбы от метро «Водный стадион» и 10 мин. от новой станции МЦК «Балтийская». Недалеко от жилого комплекса проходит основная магистраль города – Ленинградское шоссе и Третье транспортное кольцо. На автомобиле из центра Москвы до «Невского» можно доехать, следуя по Ленинградскому шоссе, далее повернув на ул. Выборгская.
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss">
    .portfolio-typical{
        &-body{
            margin-top: 91px;
            margin-bottom: 80px;

            h1.title{
                margin-bottom: 63px;
                flex-basis: 100%;
            }

            h4.title{
                max-width: 515px;
                margin-bottom: 15px;
            }
        }

        &-block{
            display: flex;
            flex-direction: row-reverse;
            justify-content: space-between;
            margin-bottom: 35px;

            @media screen and (max-width: 1200px){
                flex-direction: column-reverse;
            }
        }

        &-left{
            max-width: 535px;

            @media screen and (max-width: 1200px){
                max-width: 100%;
            }
        }

        &-right{
            @media screen and (max-width: 1200px){
                margin-bottom: 35px;
            }

            &__img{
                @media screen and (max-width: 600px){
                    max-width: 100%;
                }
            }
        }
    }

</style>