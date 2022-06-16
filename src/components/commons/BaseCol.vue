<template>
    <div class="col">
        <h5 class="col__title">{{col.title}}</h5>
        <div class="col__products">
            <div class="row" v-for="(product, i) in col.products" :key="i">
                <div class="row__info">
                    <span class="row__name">{{product.name}}</span>
                    <div class="row__stars" v-show="product.isStar">
                        <i v-for="i in 5" :key="i" class="fa-solid fa-star"></i>
                    </div>
                    <span class="row__promo-price" v-show="product.promoPrice">{{product.promoPrice}}</span>
                    <span class="row__price" v-show="product.price">{{product.price}}</span>
                    <small class="row__creator" v-show="product.creator">{{product.creator}}</small>
                </div>
                <div class="row__image">
                    <img class="row__img" :src="require(`../../assets/img/${product.src}`)" :alt="product.name">
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'BaseCol',
        props: {
            col: Object
        }
    }
</script>

<style lang="scss" scoped>
    @import '../../assets/style/mixins.scss';

    .col {
        display: flex;
        flex-direction: column;
        color: var(--septenary-color-text);

        &__title {
            text-transform: uppercase;
            color: var(--septenary-color-text);
            font-weight: 500;
            margin-bottom: 1.875rem; 
        }

        .row {
            @include dflex(space-between);
            align-items: flex-start;
            border-bottom: 1px solid var(--primary-bg-color);
            padding: .625rem 0;
            
            &__info {
                font-size: .875rem;
                line-height: 1.5625rem;

                span {
                    display: inline-block;
                }
            }

            &__name {
                margin-right: .3125rem;
            }

            &__stars {
                color: var(--quaternary-color-text);
            }

            &__promo-price {
                text-decoration: line-through;
                margin-right: .3125rem;
            }

            &__price {
                text-decoration: underline;
            }

            &__promo-price,
            &__price {
                font-weight: 600;
                color: var(--secondary-color-text);
            }

            &__img {
                height: 5rem;
            }
        }
    }
</style>