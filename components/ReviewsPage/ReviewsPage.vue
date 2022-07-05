<template lang="pug">
    .reviews-page
        h1.title Отзывы
        .reviews-page-container
            .reviews-page-block(v-for="(item, i) in items" :key="i")
                ReviewsPageItem(:reviews="item")
            paginate(
                v-model="page"
                :pageCount="pageCount"
                :containerClass="'blog-pagination'"
                :next-class="'blog-pagination-button'"
                :next-text="'_'"
                :page-class="'blog-pagination-item'"
                :active-class="'acitive'"
                :prev-text="''"
                :prev-class="'prev'"
                :clickHandler="pageChangeHandler"
            )
</template>

<script>
import paginationRivewsMixin from '@/mixins/pagination-reviews.mixin'
    export default {
        mixins: [paginationRivewsMixin],
        props: [],
        data(){
            return{
                reviewsItems:[
                    {
                        img: '/avatar/avatar1.jpg',
                        nameTitle: 'Сыпченко Владимир Евгеньевич',
                        text: 'В районе хорошо развита социальная и транспортная инфраструктура. В пешей доступности находятся детские сады, школы, поликлиники, магазины и фитнес-клубы. Рядом расположены живописные зелёные зоны — Волжский бульвар, обширный Кузьминский лесопарк, пруд Садки, а также музей-усадьба Кусково. Поблизости — ТЦ «Город», «Леруа Мерлен», кинотеатр «Олимпик Синема» и стадион «Москвич».',
                        date: '12 марта 2020',
                        ifImg: true,
                        subImg: [
                            '/img/thanks.png',
                            '/img/thanks.png'
                        ],
                    },
                    {
                        img: '/avatar/avatar3.png',
                        nameTitle: 'Иванов Геннадий Петрович',
                        text: 'В районе хорошо развита социальная и транспортная инфраструктура. В пешей доступности находятся детские сады, школы, поликлиники, магазины и фитнес-клубы. Рядом расположены живописные зелёные зоны — Волжский бульвар, обширный Кузьминский лесопарк, пруд Садки, а также музей-усадьба Кусково. Поблизости — ТЦ «Город», «Леруа Мерлен», кинотеатр «Олимпик Синема» и стадион «Москвич».',
                        date: '12 марта 2020',
                        ifImg: false,
                        subImg: [
                            '/img/thanks.png'
                        ],
                    },
                    {
                        img: '/avatar/avatar4.png',
                        nameTitle: 'Третьякова Анна Сергеевна',
                        text: 'В районе хорошо развита социальная и транспортная инфраструктура. В пешей доступности находятся детские сады, школы, поликлиники, магазины и фитнес-клубы. Рядом расположены живописные зелёные зоны — Волжский бульвар, обширный Кузьминский лесопарк, пруд Садки, а также музей-усадьба Кусково. Поблизости — ТЦ «Город», «Леруа Мерлен», кинотеатр «Олимпик Синема» и стадион «Москвич».',
                        date: '12 марта 2020',
                        ifImg: true,
                        subImg: [
                            '/img/thanks.png'
                        ],
                    },
                    {
                        img: '/avatar/avatar4.png',
                        nameTitle: 'Третьякова Анна Сергеевна',
                        text: 'В районе хорошо развита социальная и транспортная инфраструктура. В пешей доступности находятся детские сады, школы, поликлиники, магазины и фитнес-клубы. Рядом расположены живописные зелёные зоны — Волжский бульвар, обширный Кузьминский лесопарк, пруд Садки, а также музей-усадьба Кусково. Поблизости — ТЦ «Город», «Леруа Мерлен», кинотеатр «Олимпик Синема» и стадион «Москвич».',
                        date: '12 марта 2020',
                        ifImg: true,
                        subImg: [
                            '/img/thanks.png'
                        ],
                    },
                    {
                        img: '/avatar/avatar4.png',
                        nameTitle: 'Третьякова Анна Сергеевна',
                        text: 'В районе хорошо развита социальная и транспортная инфраструктура. В пешей доступности находятся детские сады, школы, поликлиники, магазины и фитнес-клубы. Рядом расположены живописные зелёные зоны — Волжский бульвар, обширный Кузьминский лесопарк, пруд Садки, а также музей-усадьба Кусково. Поблизости — ТЦ «Город», «Леруа Мерлен», кинотеатр «Олимпик Синема» и стадион «Москвич».',
                        date: '12 марта 2020',
                        ifImg: true,
                        subImg: [
                            '/img/thanks.png'
                        ],
                    },
                ]
            }
        },


        mounted(){
            this.setupPagination(this.reviewsItems)
            console.log(this.reviewsItems.subImg);
        }
    }
</script>

<style lang="scss">
    .reviews-page{
        margin-top: 91px;
        margin-bottom: 80px;
        .title{
            margin-bottom: 60px;
        }

        &-container{
            margin-bottom: 10px;
        }

        &-block{
            margin-bottom: 40px;
        }
    }
</style>
