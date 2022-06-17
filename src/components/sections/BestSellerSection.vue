<template>
    <section class="best-seller">
        <div class="container">
            <BaseTitle title="Best Seller" text="Must have products from our top sellers"/>
            <div class="best-seller__box">
                <div class="best-seller__scroll">
                    <i class="fa-solid fa-chevron-left"></i>
                </div>
                <div class="best-seller__images" v-for="(image, i) in images" :key="i">
                    <img class="best-seller__img" :src="require(`../../assets/img/${image}`)">
                    <div class="best-seller__overlay">
                        <span class="best-seller__overlay-text"><i class="fa-regular fa-square-check"></i></span>
                    </div>
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
            position: relative;
            margin: .3125rem;

            &:hover .best-seller__overlay {
                background: linear-gradient(to bottom, rgba(66,126,209, 0.8) 0%, rgba(226,130,178, 1) 100%);
            }

            &:hover .best-seller__overlay-text {
                display: block;
            }
        }

        &__overlay {
            @include dflex(center);
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            text-align: center;
            
            &-text {
                padding: .8125rem 1.0625rem;
                background-color: var(--quaternary-bg-color);
                color: var(--primary-color-text);
                border-radius: 50%;
                font-size: 1.25rem;
                cursor: pointer;
                display: none;
            }
        }
    }
</style>