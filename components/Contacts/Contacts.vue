<template lang="pug">
    .contacts
        h1.title Контакты
        ContactsOnMap(:contactsInfo="contacts.contactsInfo" :contactsMap="contacts.contactsMap")
        ContactsRest
</template>

<script>
    export default {
        // props: ['contacts'],
        data(){
            return {
                contacts: {
                    contactsInfo:[
                        {
                            "label": "Адрес:",
                            "text": "г. Смоленск, ул. Пушкина, д. 123"
                        },
                        {
                            "label": "Телефон:",
                            "text": "+7 (888) 555-35-35"
                        },
                        {
                            "label": "Время работы:",
                            "text": "ПН–ПТ: 09:00 — 18:00 СБ–ВС: Выходной"
                        }
                    ],
                    contactsMap: "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2300.7627694747493!2d32.029962916061315!3d54.78413697374479!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x46cef7ffb110cc1b%3A0xbde9737672433232!2z0YPQuy4g0J_Rg9GI0LrQuNC90LAsIDEyMywg0KHQvNC-0LvQtdC90YHQuiwg0KHQvNC-0LvQtdC90YHQutCw0Y8g0L7QsdC7LiwgMjE0MDAw!5e0!3m2!1sru!2sru!4v1611937339233!5m2!1sru!2sru",
                    rest:[
                        {
                            "title": "Отдел продаж",
                            "phone": "+7 888 555 35 35",
                            "eMail": "smolconstruction@mail.ru"
                        },
                        {
                            "title": "Технический отдел",
                            "phone": "+7 888 555 35 35",
                            "email": "smolconstruction@mail.ru"
                        }
                    ]
                }
            }
        }
    }
</script>

<style lang="scss">
    .contacts{
        margin-top: 91px;
        margin-bottom: 103px;
        .title{
            margin-bottom: 60px;
        }

        @media screen and (max-width: 600px){
            margin-bottom: 80px;
        }
    }
</style>
