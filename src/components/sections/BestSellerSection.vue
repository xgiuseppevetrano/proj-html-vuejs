<template>
    <section class="best-seller">
        <div class="container">
            <BaseTitle title="Best Seller" text="Must have products from our top sellers"/>
            <div class="best-seller__box">
                <div class="best-seller__scroll">
                    <i class="fa-solid fa-chevron-left"></i>
                </div>
                <BaseImage v-for="(image, i) in images" :key="i" :image="image"/>
                <div class="best-seller__scroll">
                    <i class="fa-solid fa-chevron-right"></i>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    import BaseTitle from '../commons/BaseTitle.vue';
    import BaseImage from '../commons/BaseImage.vue';

    export default {
        name: 'BestSellerSection',
        components: {
            BaseTitle,
            BaseImage
        },
        data() {
            return {
                images: [
                    {
                        src: 'spring_printed_dress-200x260.jpg',
                        name: 'Spring Dress',
                        category: 'Woman, Dress',
                        price: '$47',
                    },
                    {
                        src: 'modern_love_tee-200x260.jpg',
                        name: 'Modern Love Tee',
                        category: 'Woman, T-shirt',
                        price: '$68',
                    },
                    {
                        src: 'black_leather_jacket-200x260.jpg',
                        name: 'Black Leather Jacket',
                        category: 'Man, Jacket',
                        price: '$200',
                    },
                    {
                        src: 'black_elegant_leather_jacket-200x260.jpg',
                        name: 'Black Elegant Jacket',
                        category: 'Woman, Jacket',
                        price: '$125',
                    },
                    {
                        src: 'hipster_black_top-200x260.jpg',
                        name: 'Hipster Black Top',
                        category: 'Woman, T-shirt',
                        price: '57$',
                    },
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
    }
</style>