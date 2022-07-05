<template lang="pug">
    .privacy-policy
        h1.title Политика конфиденциальности
        PrivacyPolicyText
        PrivacyPolicyList
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss">
    .privacy-policy{
        margin-top: 91px;
        margin-bottom: 83px;

        .title{
            margin-bottom: 64px;
            width: 861px;

            @media screen and (max-width: 1200px){
                width: auto;
            }

            @media screen and (max-width: 600px){
                width: 100%;
                word-wrap: break-word;
            }
        }

        @media screen and (max-width: 600px){
            margin-bottom: 80px;
        }
    }
</style>