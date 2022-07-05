<template lang="pug">
    .overhaul
        .overhaul-left
            h3.title Особенности капитального ремонта
            p.sub-title Капитальный ремонт требует наличия большого количество времени, сил и денежных средств, а так же наличия специальной техники и умений. Особенностью выполнения капитального ремонта выступает выполнение ремонтных работ на всей площади квартиры, заменой всех систем коммуникации и внешнего вида помещения. В случае необходимости выполнения перепланировки квартиры необходимо согласовать план ремонтных работ с официальными органами, так же в процессе замены электрических систем необходимо соблюдать технологии ремонта.
        .overhaul-right
            img(src="/img/overHaulImg.png").overhaul-right__img
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss">
    .overhaul{
        display: flex;
        flex-direction: row-reverse;
        justify-content: space-between;
        margin-bottom: 60px;

        @media screen and (max-width: 1200px){
            flex-direction: column-reverse;
        }

        @media screen and (max-width: 600px){
            margin-bottom: 40px;
        }

        &-left{
            max-width: 538px;
            
            @media screen and(max-width: 1200px){
                max-width: 100%;
            }

            .title{
                margin-bottom: 20px;
                @media screen and (max-width: 1200px){
                    
                }
            }

            .sub-title{
                max-width: 535px;

                @media screen and(max-width: 1200px){
                    max-width: 100%;
                    margin-bottom: 60px;
                }
            }
        }

        &-right{
            border-radius: 4px;
            @media screen and (max-width: 1200px){
                margin-bottom: 40px;
            }

            @media screen and (max-width: 600px){
                margin-bottom: 30px;
            }

            &__img{
                @media screen and (max-width: 600px){
                    max-width: 100%;
                }
            }
        }
    }
</style>