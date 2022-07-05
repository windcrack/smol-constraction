<template lang="pug">
    .company-services-body
        .claster
        img(:src="serv.img").company-services-img
        h5.title {{serv.title}}
</template>

<script>
    export default {
        props:['serv']
    }
</script>

<style lang="scss">
.company-services-body{
    position: relative;
    background: #F8F8FF;
    width: 350px;
    height: 250px;
    border: 1px solid #F8F8FF;
    box-sizing: border-box;
    border-radius: 0px 30px;
    padding: 38px 40px 0;
    overflow: hidden;

    @media screen and (max-width: 1200px){
        width: 330px !important;
    }

    @media screen and (max-width: 600px){
        margin-top: auto;
        width: 284px !important; 
        padding-bottom: 40px;
        display: flex;
        flex-direction: column;
        height: auto;
        padding-bottom: 40px;
    }

    &:hover{
        .claster{
            opacity: 1;
        }
    }
}

.company-services-img{
    margin-bottom: 20px;

    @media screen and (max-width: 600px){
        width: 60px;
    }
}
            
</style>