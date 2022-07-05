<template lang="pug">
    .services
        h1.title Услуги
        .services-wrapper
            .services-container(v-for="(item, i) in servicesItems" :key="i")
                ServicesPageBlock(:serv="item")
</template>

<script>
    export default {
        data(){
            return{
                servicesItems:[
                    {
                        title:'Строительство промышленной недвижимости', 
                        descr: 'Все объекты тщательно проверяются, чтобы минимизировать риски наших клиентов.'
                    },
                    {
                        title:'Строительство промышленной недвижимости', 
                        descr: 'Проект строительства доходных домов — виды и особенности'
                    },
                    {
                        title:'Строительство жилой недвижимости', 
                        descr:'Строительство мелких и крупных жилых комплексов, частных домов'
                    },
                    {
                        title:'Ремонт промышленной недвижимости', 
                        descr:'«Эксклюзивные» объекты и условия, наиболее выгодные предложения'
                    },
                    {
                        title:'Ремонт коммерческой недвижимости', 
                        descr:'Ремонт коммерческой недвижимости достаточно похож на отделку жилья'
                    },
                    {
                        title:'Ремонт жилой недвижимости', 
                        descr:'Ремонтные работы, которые направлены на улучшение общего состояния квартиры'
                    },
                ]
            }
        }
    }
</script>

<style lang="scss">
    .services{
        margin-top: 91px;
        &-wrapper{
            display: flex;
            flex-wrap: wrap;
            margin-top: 60px;
            justify-content: space-between;
        }
        &-container{
            margin-bottom: 40px;
        }
    }
</style>