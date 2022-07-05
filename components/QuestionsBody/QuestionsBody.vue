<template lang="pug">
    .questions-body
        .questions-header(@click="toggle")
            h6.title {{quest.title}}
            .questions-header__minus(v-if="togglerBlock") -
            .questions-header__plus(v-else) +
        transition(name="fade")
            .questions-answer(v-show="togglerBlock")
                p.sub-title {{quest.answer}}
</template>

<script>
    export default {
        props: ['quest'],
        data(){
            return{
                togglerBlock: false,
            }
        },

        methods:{
            toggle(){
                this.togglerBlock = !this.togglerBlock;
            }
        }
    }
</script>

<style lang="scss">
    .questions-body{
        max-width: 540px;
        background: #FFFFFF;
        border-radius: 2px;
        margin-bottom: 15px;

        @media screen and (max-width: 1200px){
            max-width: 689px;
        }

        @media screen and (max-width: 600px){
            max-width: 285px;
        }
    }

    .questions-header{
        box-shadow: 0px 7px 20px rgba(0, 0, 0, 0.05);
        height: 55px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 0 24px; 

        .title{
            margin: 0;
        }

        &__plus, &__minus{
            color: #22917B;
            font-size: 24px;
        }
    }

    .questions-answer{
        padding: 16px 20px 16px 24px; 
    }
</style>