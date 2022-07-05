<template lang="pug">
    .construction-stages
        h2.title.title_margin21 Этапы строительства
        p.sub-title.sub-title_bottom50.sub-title_width824 Строительная компания берет на себя ответственность за все этапы выполнения работ: от проектных до отделочных, а будущий владелец только выбирает или утверждает проект и принимает готовое к эксплуатации здание. 
        .construction-wrapper
            .construction-items(v-for="item in constrItem" :key="item.num")
                ConstructionStagesBody(:constr="item")
        button.button.button_color.button_radius30.button_width229.button_border-green(v-scroll-to="'#appli'")
            span.button__text оставить заявку
</template>

<script>
    export default {
        data(){
            return{
                constrItem:[
                    {
                        num: '1',
                        title: 'Общестроительные работы',
                        subTitle: 'Устройство фундамента и подвала. Возведение стен и крыши',
                    },
                    {
                        num: '2',
                        title: 'Установка окон, дверей, утепления',
                        subTitle: 'Монтаж с  использованием  необходимых комплектующих',
                    },
                    {
                        num: '3',
                        title: 'Разводка и монтаж коммуникаций',
                        subTitle: 'Прокладка труб, монтаж котельного оборудования и установка сантехники',
                    },
                    {
                        num: '4',
                        title: 'Внутренние отделочные работы',
                        subTitle: 'Отделка внутренних и внешних поверхностей здания',
                    }
                ]
            }
        }
    }
</script>

<style lang="scss">
    .construction-stages{
        margin-bottom: 90px;
    }

    .construction-wrapper{
        display: flex;
        justify-content: space-between;
        
        @media (max-width: 1200px){
            flex-wrap: wrap;
        }

        @media (max-width: 600px){
            margin-top: 40px;
        }
    }

    .construction-items{
        &:last-child{
            .arrow-long{
                display: none;
            }
        }

        @media (max-width: 1200px){
            flex-basis: 50%;
        }

        @media (max-width: 600px){
            flex-basis: 100%;
        }
    }

</style>