<template>
    <div>
        <div class="card__overlay">
            <img class="card__img" :src="require(`../../assets/img/${card.src}`)" :alt="card.title">
            <div class="card__overlay-element">
                <span class="card__overlay-text"><i class="fa-regular fa-square-check"></i></span>
            </div>
        </div>
        <h4 class="card__title">{{card.title}}</h4>
        <small class="card__category">{{card.category}}</small>
        <div>
            <small class="card__sale" v-show="card.salePrice">{{card.salePrice}}</small>
            <span class="card__price">{{card.price}}</span>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'BaseCard',
        props: {
            card: Object
        },
    }
</script>

<style lang="scss" scoped>
    @import '../../assets/style/mixins.scss';

    .card {
        line-height: 1.5625rem;

        &__title {
            color: var(--secondary-color-text);
        }

        &__category {
            color: var(--tertiary-color-text);
        }

        &__sale {
            text-decoration: line-through;
            margin-right: .625rem;
        }

        &__sale,
        &__price {
            color: var(--quaternary-color-text);
        }

        &__overlay {
            position: relative;

            &-element {
                @include dflex(center);
                position: absolute;
                top: 0;
                left: 0;
                right: 0;
                bottom: 0;
                text-align: center;
            }

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

        &__hover:hover &__overlay-element {
            background: linear-gradient(to bottom, rgba(66,126,209, 0.8) 0%, rgba(226,130,178, 1) 100%);
        }

        &__hover:hover &__overlay-text {
            display: block;
        }
    }
</style>