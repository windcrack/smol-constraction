<template lang="pug">
    .blog-page
        h1.title Блог
        .blog-page-wrapper
            .blog-page-items(v-for="(item, i) in items" :key="i")
                BlogPageBody(:text="item")
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
import paginationBlogMixin from '@/mixins/pagination-blog.mixin'
    export default {
        mixins: [paginationBlogMixin],
        data(){
            return{

                blogItems:[
                    {
                        title: 'Жилой район «Волжский парк»',
                        descr: 'В районе хорошо развита социальная и транспортная инфраструктура. В пешей доступности находятся детские сады, школы, поликлиники, магазины и фитнес-клубы. Рядом расположены живописные зелёные зоны — Волжский бульвар, обширный Кузьминский лесопарк, пруд Садки, а также музей-усадьба Кусково. Поблизости',
                        date: '12 декабря 2020',
                        category: 'Строительство'
                    },
                    {
                        title: 'Жилой район «Волжский парк»',
                        descr: 'В районе хорошо развита социальная и транспортная инфраструктура. В пешей доступности находятся детские сады, школы, поликлиники, магазины и фитнес-клубы. Рядом расположены живописные зелёные зоны — Волжский бульвар, обширный Кузьминский лесопарк, пруд Садки, а также музей-усадьба Кусково. Поблизости',
                        date: '12 декабря 2020',
                        category: 'Ремонт'
                    },
                    {
                        title: 'Жилой район «Волжский парк»',
                        descr: 'В районе хорошо развита социальная и транспортная инфраструктура. В пешей доступности находятся детские сады, школы, поликлиники, магазины и фитнес-клубы. Рядом расположены живописные зелёные зоны — Волжский бульвар, обширный Кузьминский лесопарк, пруд Садки, а также музей-усадьба Кусково. Поблизости',
                        date: '12 декабря 2020',
                        category: 'Новости компании'
                    },
                    {
                        title: 'Жилой район «Волжский парк»',
                        descr: 'В районе хорошо развита социальная и транспортная инфраструктура. В пешей доступности находятся детские сады, школы, поликлиники, магазины и фитнес-клубы. Рядом расположены живописные зелёные зоны — Волжский бульвар, обширный Кузьминский лесопарк, пруд Садки, а также музей-усадьба Кусково. Поблизости',
                        date: '12 декабря 2020',
                        category: 'Новости компании'
                    },
                    {
                        title: 'Жилой район «Волжский парк»',
                        descr: 'В районе хорошо развита социальная и транспортная инфраструктура. В пешей доступности находятся детские сады, школы, поликлиники, магазины и фитнес-клубы. Рядом расположены живописные зелёные зоны — Волжский бульвар, обширный Кузьминский лесопарк, пруд Садки, а также музей-усадьба Кусково. Поблизости',
                        date: '12 декабря 2020',
                        category: 'Отделка'
                    },
                    {
                        title: 'Жилой район «Волжский парк»',
                        descr: 'В районе хорошо развита социальная и транспортная инфраструктура. В пешей доступности находятся детские сады, школы, поликлиники, магазины и фитнес-клубы. Рядом расположены живописные зелёные зоны — Волжский бульвар, обширный Кузьминский лесопарк, пруд Садки, а также музей-усадьба Кусково. Поблизости',
                        date: '12 декабря 2020',
                        category: 'Отделка'
                    },
                ]
            }
        },

        methods:{
            clickPage(){
                console.log('Hello');
            }
        },

        mounted(){
            this.setupPagination(this.blogItems)
        }
    }
</script>

<style lang="scss">
    .blog-page{
        margin: 91px 0;
        &-wrapper{
            margin-top: 60px;
            width: 918px;

            @media screen and (max-width: 1200px){
                width: 688px;
            }

            @media screen and (max-width: 600px){
                max-width: 281px;
            }
        }

        &-items{
            margin-bottom: 50px;
        }
    }
</style>
