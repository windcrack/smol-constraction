<template lang="pug">
    .arrow-up(v-scroll-to="'#up'" v-if='scrollTop > 1000')
        img(src="arrowUp.svg")
</template>

<script>
    export default {
        data(){
            return{
                scrollTop: 0,
            }
        },
        mounted(){
            window.addEventListener('scroll', ()=>{
                this.scrollTop = window.pageYOffset || document.documentElement.scrollTop
            })
        }
    }
</script>

<style lang="scss">
    .arrow-up{
        position: fixed;
        right: 1rem;
        bottom: 1rem;
        background: linear-gradient(50.2deg, #22917B 12.16%, #22B573 92.67%);
        border: 1px solid #F2F6F7;
        box-sizing: border-box;
        border-radius: 25px 0;
        display: flex;
        justify-content: center;
        align-items: center;

        width: 56px;
        height: 56px;
        align-self: flex-start;
        z-index: 1;

        cursor: pointer;

        @media (max-width: 1200px){
            display: none;
        }
    }
</style>