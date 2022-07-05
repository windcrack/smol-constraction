<template lang="pug">
    .our-partners
        h1.title Наши партнеры
        ClientList
        PartnerList
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss">
    .our-partners{
        margin-top: 91px;
        margin-bottom: 103px;

        @media screen and (max-width: 600px){
            margin-bottom: 80px;
        }

        .title{
            margin-bottom: 60px;
        }
    }
</style>