<template lang="pug">
    .privacy-list
        ol.privacy-list-items
            li.privacy-list-item Персональная информация пользователей, которую получает и обрабатывает ООО «Сноб Медиа»
                ol.privacy-list-items
                    li.privacy-list-item В рамках настоящей Политики под «персональной информацией пользователя» понимаются:
                        ol.privacy-list-items
                            li.privacy-list-item Персональная информация, которую пользователь предоставляет о себе самостоятельно при регистрации (создании учетной записи) или в процессе использования Сервисов, включая персональные данные пользователя. Обязательная для предоставления Сервисов (оказания услуг) информация помечена специальным образом. Иная информация предоставляется пользователем на его усмотрение.
                            li.privacy-list-item Данные, которые автоматически передаются Сервисам в процессе их использования с помощью установленного на устройстве пользователя программного обеспечения, в том числе IP-адрес, информация из cookie, информация о браузере пользователя (или иной программе, с помощью которой осуществляется доступ к Сервисам), время доступа, адрес запрашиваемой страницы.
                            li.privacy-list-item Иная информация о пользователе, в случае, если ее сбор и/или предоставление определено в регулирующих документах отдельных Сервисов.
                    li.privacy-list-item Настоящая Политика применима только к Сервисам ООО «Сноб Медиа». ООО «Сноб Медиа» не контролирует и не несет ответственность за сайты третьих лиц, на которые пользователь может перейти по ссылкам, доступным на сайтах ООО «Сноб Медиа». На таких сайтах у пользователя может собираться или запрашиваться иная персональная информация, а также могут совершаться иные действия.
                    li.privacy-list-item ООО «Сноб Медиа»в общем случае не проверяет достоверность персональной информации, предоставляемой пользователями, и не осуществляет контроль за их дееспособностью. Однако ООО «Сноб Медиа» исходит из того, что пользователь предоставляет достоверную и достаточную персональную информацию по вопросам, предлагаемым в форме регистрации, что указанные им при регистрации персональные данные принадлежат лично ему и поддерживает эту информацию в актуальном состоянии. Риск предоставления недостоверной информации несет предоставивший ее пользователь.
                    li.privacy-list-item Согласие пользователя на обработку персональных данных действует бессрочно с момента осуществления регистрации пользователя на сайте, и не требует периодического подтверждения. ООО «Сноб Медиа» будет хранить персональную информацию столько времени, сколько это необходимо для достижения цели, для которой она была собрана, или для соблюдения требований законодательства и нормативных актов.
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss">
    .privacy-list{
        font-weight: 300;
        font-size: 16px;
        line-height: 26px;
        color: #292929;
    }

    .privacy-list{
        &-items{
            list-style: none;
            counter-reset: li;
            padding-left: 14px;

            @media screen and (max-width: 600px){
                padding-left: 0px;
            }
            
        }

        &-item{
            padding-bottom: 5px;
            &:before{
                counter-increment: li;
                content: counters(li,".") ". ";
                color: #22917B;
            }

            @media screen and (max-width: 600px){
                padding-bottom: 8px;
            }
        }
    }
</style>