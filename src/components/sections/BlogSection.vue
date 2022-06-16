<template>
    <section class="blog">
        <div class="container">
            <BaseTitle title="From Our Blog" text="The latest Classic Shop news"/>
            <div class="blog__cards">
                <BlogCard class="blog__card" v-for="(card, i) in cards" :key="i" :card="card"/>
            </div>
        </div>
    </section>
</template>

<script>
    import BaseTitle from '../commons/BaseTitle.vue'
    import BlogCard from '../commons/BlogCard.vue'

    export default {
        name: 'BlogSection',
        components: {
            BaseTitle,
            BlogCard
        },
        data() {
            return {
                cards: [
                    {
                        src: 'post_img_12-320x202.jpg',
                        title: 'Aenean lobortis sapien enim viverra',
                        info: 'September 9th,2015 | 0 Comments',
                        text: 'Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla.'
                    },
                    {
                        src: 'post_img_11-320x202.jpg',
                        title: 'Duis ac massa semper maximus',
                        info: 'September 9th,2015 | 0 Comments',
                        text: 'Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla.'
                    },
                    {
                        src: 'post_img_10-320x202.jpg',
                        title: 'Nunc fermit nulla eu justo sem id',
                        info: 'September 9th,2015 | 0 Comments',
                        text: 'Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla.'
                    },

                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
    @import '../../assets/style/mixins.scss';

    .blog {
        margin: 5rem 0;

        &__cards {
            @include dflex(center);
            margin-top: 2.5rem;
        }

        &__card {
            width: calc(100% / 3 - 1.875rem);
            margin: 0 .9375rem;
        }
    }
</style>