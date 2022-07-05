<template lang="pug">
    .bread-crums
        ul.bread-crums-items
            li.bread-crums-item
                nuxt-link(to="/").bread-crums-link Главная
            li.bread-crums-item
                nuxt-link(to="/about").bread-crums-link.bread-crums-link_active О компании
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss">
    .bread-crums{
        font-weight: 300;
        font-size: 16px;
        line-height: 26px;
        color: #333333;
        transform: translate(0, 50px);

        &-items{
            display: flex;
            margin-left: 0;
            padding-left: 0;
        }

        &-item{
            list-style-type: square;
            margin-right: 28px;

            &::marker{
                color: #000;
            }

            &:first-child{
                list-style-type: none;
            }

            
        }

        &-link{
            &_active{
                opacity: 0.5;
            }
        }
    }
</style>