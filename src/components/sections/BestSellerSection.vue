<template>
    <section class="best-seller">
        <div class="container">
            <BaseTitle title="Best Seller" text="Must have products from our top sellers"/>
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
        </div>
    </section>
</template>

<script>
    import BaseTitle from '../commons/BaseTitle.vue'

    export default {
        name: 'BestSellerSection',
        components: {
            BaseTitle
        },
        data() {
            return {
                images: [
                    'spring_printed_dress-200x260.jpg',
                    'modern_love_tee-200x260.jpg',
                    'black_leather_jacket-200x260.jpg',
                    'black_elegant_leather_jacket-200x260.jpg',
                    'hipster_black_top-200x260.jpg'
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
    @import '../../assets/style/mixins.scss';

    .best-seller {
        margin: 5rem 0;

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
            margin: .3125rem;
        }
    }
</style>