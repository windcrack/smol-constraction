<template lang="pug">
    .constraction-body
        .constraction-block
           .constraction-block__nubmer {{constr.num}}
           img(src="arrowLong.svg").arrow-long
        h6.title {{constr.title}}
        p.sub-title {{constr.subTitle}}
</template>

<script>
    export default {
        props:['constr']
    }
</script>

<style lang="scss">
    .constraction-body{
        max-width: 212px;
        margin-bottom: 55px;
    }

    .constraction-block{
        display: flex;
        justify-content: space-between;
        margin-bottom: 25px;

        @media screen and (max-width: 600px){
            // flex-direction: column;
        }

        &__nubmer{
            color: #22917B;
            border: 1px solid #22917B;
            border-radius: 50%;
            width: 65px;
            height: 65px;
            display: flex;
            justify-content: center;
            align-items: center; 
        }
    }

    .title{
        margin-bottom: 9px;
    }
</style>