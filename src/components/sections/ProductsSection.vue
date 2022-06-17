<template>
    <section class="products">
        <div class="container">
            <div class="products__box">
                <BaseCol class="products__col col" v-for="(col, i) in cols" :key="i" :col="col"/>
            </div>
        </div>
    </section>
</template>

<script>
    import BaseCol from '../commons/BaseCol.vue'

    export default {
        name: 'ProductsSection',
        components: {
            BaseCol
        },
        data() {
            return {
                cols: [
                    {
                        title: 'Featured',
                        products: [
                            {
                                name: 'Black Jacket',
                                isStar: false,
                                price: '$125',
                                src: 'black_leather_jacket-120x156.jpg',
                            },
                            {
                                name: 'Black Leather Jacket',
                                isStar: true,
                                promoPrice: '$235',
                                price: '$200',
                                src: 'black_elegant_leather_jacket-120x156.jpg',
                            },
                            {
                                name: 'Hipster Black Top',
                                isStar: false,
                                price: '$57',
                                src: 'hipster_black_top-120x156.jpg',
                            },

                        ]
                    },
                    {
                        title: 'On sale',
                        products: [
                            {
                                name: 'Black Leather Jacket',
                                isStar: true,
                                promoPrice: '$235',
                                price: '$200',
                                src: 'black_elegant_leather_jacket-120x156.jpg',
                            },
                            {
                                name: 'Blue Leather Jacket',
                                isStar: false,
                                promoPrice: '$80',
                                price: '$60',
                                src: 'blue_leather_jacket-120x156.jpg',
                            },
                            {
                                name: 'Modern Leather Boots',
                                isStar: false,
                                promoPrice: '$50',
                                price: '$30',
                                src: 'modern_leather_boots-120x156.jpg',
                            },

                        ]
                    },
                    {
                        title: 'Top rated',
                        products: [
                            {
                                name: 'Leather Gloves',
                                isStar: true,
                                price: '$45',
                                src: 'leather_gloves-120x156.jpg',
                            },
                            {
                                name: 'Black Leather Jacket',
                                isStar: true,
                                promoPrice: '$235',
                                price: '$200',
                                src: 'black_elegant_leather_jacket-120x156.jpg',
                            },
                            {
                                name: 'Spring Printed Dress',
                                isStar: true,
                                price: '$47',
                                src: 'spring_printed_dress-120x156.jpg',
                            },

                        ]
                    },
                    {
                        title: 'Leatest review',
                        products: [
                            {
                                name: 'Black Leather Jacket',
                                isStar: true,
                                creator: 'by admin',
                                src: 'black_elegant_leather_jacket-120x156.jpg',
                            },
                            {
                                name: 'Leather Gloves',
                                isStar: true,
                                creator: 'by Beardman',
                                src: 'leather_gloves-120x156.jpg',
                            },
                            {
                                name: 'Spring Printed Dress',
                                isStar: true,
                                creator: 'by admin',
                                src: 'spring_printed_dress-120x156.jpg',
                            },

                        ]
                    },


                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
    @import '../../assets/style/mixins.scss';

    .products {
        margin: 2.5rem 0;

        &__box {
            @include dflex(space-between);
        }

        &__col {
            width: calc(100% / 4 - 1.875rem);
            margin: .9375rem;
        }
    }
</style>