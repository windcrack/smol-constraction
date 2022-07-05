<template lang="pug">
    .overhaul-stages
        h3.title Этапы капитального ремонта
        p.sub-title Капитальный ремонт позволяет восстановить эстетическую привлекательность помещения и восстановить ее безопасность для проживания. Специалисты производят ремонт в следующие основные этапы:
        ol.overhaul-lists
            li(v-for="item in stagesItems" :key="item").overhaul-lists__item {{item}}
</template>

<script>
    export default {
        data(){
            return{
                stagesItems: [
                    'Создание плана проекта',
                    'Подготовительный этап',
                    'Третий этап',
                    'Заключительный этап ремонта'
                ]
            }
        }
    }
</script>

<style lang="scss">
    .overhaul-stages{
        margin-bottom: 150px;
        

        @media screen and (max-width: 600px){
            margin-bottom: 80px;
        }
        .title{
            margin-bottom: 20px;
        }

        .sub-title{
            margin-bottom: 30px;
        }
    }

    .overhaul-lists{
        margin-left: 0;
        padding-left: 12px;

        &__item{
            padding-bottom: 20px;
            font-weight: 300;
            font-size: 16px;
            line-height: 24px;
            color: #292929;
            &::marker{
                color: #22917B;
            }
        }
    }
</style>