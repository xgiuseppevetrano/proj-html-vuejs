<template>
    <div class="card">
        <img class="card__img" :src="require(`../../assets/img/${card.src}`)" :alt="card.title">
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
    .card {
        line-height: 1.5625rem;

        &__img {
            width: 100%;
        }

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
    }
</style>