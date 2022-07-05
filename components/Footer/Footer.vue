<template lang="pug">
    footer
        .container-footer
            .footer-body
                FooterLogo
                FooterLists
                FooterContacts
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss">
    footer{
        background: #333333;
        position: relative;
        z-index: 2;
    }
    .footer-body{
        margin: 56px 165px;
        display: flex;
        justify-content: space-between;

        @media screen and (max-width: 1200px){
            margin: 50px 22px 50px 40px;
            flex-wrap: wrap;
        }

        @media screen and (max-width: 600px){
            margin: 53px 17px;
        }
    }
</style>