<template>
    <section class="best-seller">
        <BaseTitle title="New Arrivals" text="Brand new products from top designers"/>
        <div class="best-seller__box">
            <div class="best-seller__scroll">
                <i class="fa-solid fa-chevron-left"></i>
            </div>
            <div class="best-seller__images">
                <img class="best-seller__img" v-for="(image, i) in images" :key="i" :src="require(`../../assets/img/${image}`)" :alt="i">
            </div>
            <div class="best-seller__scroll">
                <i class="fa-solid fa-chevron-right"></i>
            </div>
        </div>
    </section>
</template>

<script>
    import BaseTitle from '../commons/BaseTitle.vue'

    export default {
        name: 'NewArrivalsSection',
        components: {
            BaseTitle
        },
        data() {
            return {
                images: [
                    'black_elegant_leather_jacket.jpg',
                    'hipster_black_top.jpg',
                    'black_leather_suit.jpg',
                    'modern_love_tee.jpg',
                    'black_leather_jacket.jpg',
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
    @import '../../assets/style/mixins.scss';

    .best-seller {
        padding: 5rem 0;

        &__box {
            @include dflex(center);
            margin-top: 1.875rem;
        }

        &__scroll {
            padding: 1.25rem .625rem;
            background-color: var(--bg-color-scroll);
            color: var(--primary-color-text);
        }

        &__images {
            @include dflex(center);
        }

        &__img {
            width: calc(100% / 5 - 1.25rem);
            margin: .625rem;
        }
    }
</style>