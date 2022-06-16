<template>
    <section class="products">
        <div class="container">
            <BaseTitle title="Featured Products" text="Must have products from our top sellers"/>
            <RectangularButton/>
            <div class="products__cards">
                <BaseCard class="products__card" v-for="(card, index) in cards" :key="index" :card="card"/>
            </div>
        </div>
    </section>
</template>

<script>
    import BaseTitle from "../commons/BaseTitle.vue";
    import RectangularButton from "../commons/RectangularButton.vue";
    import BaseCard from "../commons/BaseCard.vue";

    export default {
        name: 'FeaturedProductsSection',
        components: {
            BaseTitle,
            RectangularButton,
            BaseCard
        },
        data() {
            return {
                cards: [
                    {
                        src: 'black_elegant_leather_jacket-200x260.jpg',
                        title: 'Black Leather Jacket',
                        category: 'Men,Jackets,Jeans',
                        salePrice: '$235',
                        price: '$200'
                    },
                    {
                        src: 'black_leather_suit-200x260.jpg',
                        title: 'Black Leather Suit',
                        category: 'Men,Jackets',
                        price: '$176'
                    },
                    {
                        src: 'blue_jacket_and_white_stripe_tee-200x260.jpg',
                        title: 'Blue Jacket & Stripe Tee',
                        category: 'Men,Jackets,Suits',
                        price: '$580'
                    },
                    {
                        src: 'modern_black_leather_suit-200x260.jpg',
                        title: 'Modern Black Leather Suit',
                        category: 'Men,Jackets',
                        price: '$96'
                    }
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
    @import '../../assets/style/mixins.scss';

    .products {
        margin: 5rem 0;

        &__cards {
            @include dflex(center);
        }

        &__card {
            margin: 0 1.875rem;
        }
    }
</style>