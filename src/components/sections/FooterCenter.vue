<template>
    <div class="footer-center">
        <div class="container">
            <div class="footer-center__box">
                <div class="footer-center__col">
                    <img class="footer-center__col-logo" src="../../assets/img/classic_shop_logo_footer.png" alt="logo img">
                    <small class="footer-center__col-address">
                        12345 North Main Street,<br>
                        New York, NY 555555<br>
                        Phone: 1.800.555.6789<br>
                        Email: info@company.com<br>
                        Web: Theme-fusion.com
                    </small>
                    <SocialNetwork class="footer-center__col-social"/>
                </div>
                <div class="footer-center__col">
                    <BaseCol class="col col-white" v-for="(col, i) in cols" :key="i" :col="col"/>
                </div>
                <div class="footer-center__col">
                    <h5 class="footer-center__col-title">Recent Posts</h5>
                    <BasePosts v-for="(post, i) in posts" :key="i" :post="post"/>
                </div>
                <div class="footer-center__col">
                    <h5 class="footer-center__col-title">Tags</h5>
                    <BaseTags v-for="(tag, i) in tags" :key="i" :tag="tag"/>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import BaseCol from '../commons/BaseCol.vue'
    import SocialNetwork from '../commons/SocialNetwork.vue'
    import BasePosts from '../commons/BasePosts.vue'
    import BaseTags from '../commons/BaseTags.vue'

    export default {
        name: 'FooterCenter',
        components: {
            SocialNetwork,
            BaseCol,
            BasePosts,
            BaseTags
        },
        data() {
            return {
                posts: [
                    'Aenean lobortis sapien enim viverra',
                    'Duis ac massa semper maximus',
                    'Nunc fermint nulla eu justo sem id',
                    'Aliquam posuere magna eget nibh',
                    'Cras ac nulla ac consecte retrum',
                    'Frusce mattis nunc ut aliquam'
                ],
                tags: [
                    'Black',
                    'boots',
                    'Brown',
                    'Casual',
                    'D&G',
                    'Fabric',
                    'flowers',
                    'Grey',
                    'hat',
                    'Hipster',
                    'lines',
                    'multi-purpose',
                    'New York',
                    'Outdoors',
                    'red',
                    'responsive',
                    'summer',
                    'sweater',
                    'Travel',
                    'Warm',
                    'White',
                    'winter',
                ],
                cols: [
                    {
                        title: 'Top rated products',
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
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
    .footer-center {
        background-color: var(--tertiary-bg-color);
        padding: 2.5rem 0;
        color: var(--quinary-color-text);

        &__box {
            display: flex;
            justify-content: space-between
        }

        &__col {
            width: calc(100% / 4 - 1.25rem);
            margin: .625rem;

            &-logo {
                height: 2.8125rem;
                margin: 1.25rem 0;
            }

            &-address {
                margin: 1.875rem 0 3.125rem;
                display: inline-block;
                line-height: 1.5625rem;
            }

            &-social {
                color: var(--quinary-color-text);
            }

            &-title {
                text-transform: uppercase;
                font-weight: 500;
                margin-bottom: 1.875rem; 
            }
        }
    }
</style>