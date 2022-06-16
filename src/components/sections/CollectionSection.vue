<template>
    <section class="big-cards">
        <BigCard class="card card--big" v-for="(card, i) in cards" :key="i" :card="card"/>
    </section>
</template>

<script>
    import BigCard from '../commons/BigCard.vue'
    export default {
        name: 'CollectionSection',
        components: {
            BigCard
        },
        data() {
            return {
                cards: [
                    {
                        src: 'winter_collection_bg.jpg',
                        title: 'Winter Collection',
                        description: 'Stylish and warm',
                        button: 'View More'
                    },
                    {
                        src: 'spring_collection_bg.jpg',
                        title: 'Spring Collection',
                        description: 'Bringht and colorful',
                        button: 'View More'
                    },
                    {
                        src: 'autumn_collection_bg.jpg',
                        title: 'Autumn Collection',
                        description: 'rich and comfortable',
                        button: 'View More'
                    }
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
    @import '../../assets/style/mixins.scss';

    .big-cards {
        padding: 5rem 0;
        @include dflex(flex-start);

        .card {
            width: calc(100% / 3);
        }
    }
</style>