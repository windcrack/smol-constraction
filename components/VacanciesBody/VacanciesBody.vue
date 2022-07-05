<template lang="pug">
    .vacancies-body
        .vacancies-header
            h3.title {{vacancy.title}}
            span.vacancies-header__sale {{vacancy.sale}}
            p.sub-title {{vacancy.subTitle}}
        span.vacancies-more(@click="toggle" v-if="!visible") Подробнее
        .vacancies-visible(v-if="visible")
            .vacancies-lists(v-for="item in vacancy.listHeader" :key="item.title")
                VacanciesList(:list="item")
            .vacancies-contact
                h5.title {{vacancy.contact.title}}
                span.vacancies-contact__name {{vacancy.contact.name}},
                label.label.label_margin тел.: 
                a(href="tel:888888888").vacancies-contact__link {{vacancy.contact.phone}},
                label.label.label_margin email.:
                a(href="mailto:").vacancies-contact__link {{vacancy.contact.email}}
</template>

<script>
    export default {
        props: ['vacancy'],
        data: ()=>({
            visible: false
        }),
        methods: {
            toggle(){
                this.visible = !this.visible
            }
        }
    }
</script>

<style lang="scss">
    .vacancies-body{
        margin-bottom: 60px;
    }

    .vacancies-header{
        display: flex;
        justify-content: space-between;
        margin-bottom: 8px;
        flex-wrap: wrap;

        @media screen and (max-width: 600px){
            flex-direction: column;
            margin-bottom: 30px;

        }

        &__sale{
            display: flex;
            align-items: center;
            justify-content: flex-end;
            flex-basis: 50%;

            @media screen and (max-width: 600px){
                flex-basis: 100%;
                justify-content: flex-start;
                order: 1;
            }
        }
    }

    .vacancies-more{
        font-weight: 500;
        font-size: 16px;
        line-height: 24px;
        text-decoration-line: underline;
        color: #22917B;
        cursor: pointer;
    }


    h3.title{
        margin-bottom: 8px;
        flex-basis: 50%;
        
        @media screen and (max-width: 600px){
            flex-basis: 100%;
            margin-bottom: 10px;
        }
    }


    h5.title{
        color: #000;
        line-height: 27px;
        margin-bottom: 15px;
    }

    .vacancies-contact{
        font-weight: 300;
        font-size: 16px;
        line-height: 26px;
        color: #333333;

        &__name{
            margin-right: 4px;
        }

        &__link{
            font-weight: 500;
            font-size: 16px;
            line-height: 24px;
            text-decoration-line: underline;
            color: #22917B;
            margin: 0 4px;
        }
    }
</style>