<template lang="pug">
    .history-body
        h5.title {{text.title}}
        p.sub-title {{text.descr}}
</template>

<script>
    export default {
        props:['text']
    }
</script>

<style lang="scss" >
    .history-body{
        color: #333333;
        margin-left: 30px;
        flex-basis: 50%;
        max-width: 540px;
    }
</style>