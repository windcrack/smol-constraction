<template lang="pug">
    .affordable
        .green-block.green-block_first
            img(src="/img/greenBlock.png")
        .green-block.green-block_second
            img(src="/img/greenBlock.png")
        h3.title Доступные цены и короткие сроки
        p.sub-title Доступные цены, быстрые сроки, знаем и соблюдаем нормы и технологии, а также — мы готовы зафиксировать финальную стоимость объекта, открытость на всех этапах, мы на связи в любое время и, конечно, индивидуальный подход к каждому клиенту!
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss">
    .affordable{
        margin: 95px auto 57px;
        position: relative;
        max-width: 822px;

        @media screen and (max-width: 1200px){
            max-width: 605px;
        }

        @media screen and (max-width: 600px){
            max-width: 244px;
        }

        .title{
            margin-bottom: 15px;
            position: relative;
            z-index: 2;
        }
    }
</style>