<template lang="pug">
    .vacancies
        h1.title Вакансии
        .vacancies-block(v-for="item in vacanciesItems" :key="item.id")
            VacanciesBody(:vacancy="item")
</template>

<script>
    export default {
        data(){
            return{
                vacanciesItems:[
                    {
                        title:'Инженер по эксплуатации',
                        sale: 'от 35 000 руб./месяц',
                        subTitle: 'Смоленск, Старомонетный переулок, 29 Опыт работы от 1 года, полная занятость',
                        listHeader: [
                            {
                                title: 'Обязанности:',
                                text: [
                                    'Контроль за соблюдением правил эксплуатации зданий, обеспечение правил противопожарной безопасности, навыки небольших ремонтных работ, редко - работы, связанные с подъемом тяжестей',
                                    'Организует подготовку ремонтных работ, определяет потребность в запасных запчастях для ремонта оборудования, по обеспечению ими предприятия.',
                                    'Осуществляет контроль над деятельностью подразделений предприятия, участвующих в проведении ремонтных работ и испытаний оборудования, за соблюдением правил эксплуатации, технического обслуживания и надзора за ним.',
                                ],
                            },
                            {
                                title: 'Требования:',
                                text: [
                                    'гражданство РФ или республики Беларусь, без в/п',
                                    'коммуникабельность, обязательность',
                                ],
                            },
                            {
                                title: 'Условия:',
                                text: [
                                    'Официальное трудоустройство, график работы плавающий',
                                    'Стандартный соц.пакет',
                                ],
                            },
                        ],
                        contact:{
                            title: 'Контакты:', 
                            name: 'Иванов Иван Иванович',
                            phone: '+7 (911) 888-88-88',
                            email: 'ivavnov@mail.ru',
                        }
                    },
                    {
                        title:'Инженер по обслуживанию зданий',
                        sale: 'по договоренности',
                        subTitle: 'Смоленск, Старомонетный переулок, 29 Опыт работы от 1 года, полная занятость',
                        listHeader: [
                            {
                                title: 'Обязанности:',
                                text: [
                                    'Контроль за соблюдением правил эксплуатации зданий, обеспечение правил противопожарной безопасности, навыки небольших ремонтных работ, редко - работы, связанные с подъемом тяжестей',
                                    'Организует подготовку ремонтных работ, определяет потребность в запасных запчастях для ремонта оборудования, по обеспечению ими предприятия.',
                                    'Осуществляет контроль над деятельностью подразделений предприятия, участвующих в проведении ремонтных работ и испытаний оборудования, за соблюдением правил эксплуатации, технического обслуживания и надзора за ним.',
                                ],
                            },
                            {
                                title: 'Требования:',
                                text: [
                                    'гражданство РФ или республики Беларусь, без в/п',
                                    'коммуникабельность, обязательность',
                                ],
                            },
                            {
                                title: 'Условия:',
                                text: [
                                    'Официальное трудоустройство, график работы плавающий',
                                    'Стандартный соц.пакет',
                                ],
                            },
                        ],
                        contact:{
                            title: 'Контакты:', 
                            name: 'Иванов Иван Иванович',
                            phone: '+7 (911) 888-88-88',
                            email: 'ivavnov@mail.ru',
                        }
                    },
                    {
                        title:'Инженер по зданию',
                        sale: '32 000 — 40 000 руб./месяц',
                        subTitle: 'Смоленск, Старомонетный переулок, 29 Опыт работы от 1 года, полная занятость',
                        listHeader: [
                            {
                                title: 'Обязанности:',
                                text: [
                                    'Контроль за соблюдением правил эксплуатации зданий, обеспечение правил противопожарной безопасности, навыки небольших ремонтных работ, редко - работы, связанные с подъемом тяжестей',
                                    'Организует подготовку ремонтных работ, определяет потребность в запасных запчастях для ремонта оборудования, по обеспечению ими предприятия.',
                                    'Осуществляет контроль над деятельностью подразделений предприятия, участвующих в проведении ремонтных работ и испытаний оборудования, за соблюдением правил эксплуатации, технического обслуживания и надзора за ним.',
                                ],
                            },
                            {
                                title: 'Требования:',
                                text: [
                                    'гражданство РФ или республики Беларусь, без в/п',
                                    'коммуникабельность, обязательность',
                                ],
                            },
                            {
                                title: 'Условия:',
                                text: [
                                    'Официальное трудоустройство, график работы плавающий',
                                    'Стандартный соц.пакет',
                                ],
                            },
                        ],
                        contact:{
                            title: 'Контакты:', 
                            name: 'Иванов Иван Иванович',
                            phone: '+7 (911) 888-88-88',
                            email: 'ivavnov@mail.ru',
                        }
                    },
                ]
            }
        }
    }
</script>

<style lang="scss">
    .vacancies{
        margin-top: 91px;
        margin-bottom: 60px;

        @media screen and (max-width: 600px){
            margin-bottom: 50px;
        }

        &-block{
            margin-top: 60px;
        }
        
        h1.title{
            color: #000;

        }
    }
</style>
