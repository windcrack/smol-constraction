<template lang="pug">
    .contacts-on-map
        iframe(:src="contactsMap" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false" tabindex="0").contacts-on-map__iframe
        ContactsBlockMap(:lists="contactsInfo")
</template>

<script>
    export default {
        props: ['contactsInfo', 'contactsMap'],
        mounted(){
            console.log(this.contactsInfo);
        }
    }
</script>

<style lang="scss">
    .contacts-on-map{
        position: relative;
        margin-bottom: 50px;

        @media screen and (max-width: 1200px){
            display: flex;
            flex-direction: column-reverse;
        }

        &__iframe{
            width: 100%;
            height: 460px;
            border-radius: 0px 40px;
            position: relative;
        }
    }
</style>
