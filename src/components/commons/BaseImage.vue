<template>
    <div class="images">
        <img class="images__img" :src="require(`../../assets/img/${image.src}`)">
        <div class="images__overlay">
            <div class="images__overlay-info">
                <h4 class="images__name">{{image.name}}</h4>
                <span class="images__category">{{image.category}}</span>
                <span class="images__price">{{image.price}}</span>
            </div>
            <div class="images__overlay-button">
                <span class="images__cart"><i class="fa-solid fa-cart-shopping"></i>Add to cart</span>
                <span class="images__details"><i class="fa-solid fa-list-ul"></i>Details</span>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'BaseImage',
        props: {
            image: Array
        }
    }
</script>

<style lang="scss" scoped>
    @import '../../assets/style/mixins.scss';

    .images {
        position: relative;
        margin: .3125rem;

        &__img {
            width: 100%;
        }

        &:hover &__overlay {
            background: linear-gradient(to bottom, rgba(66,126,209, 0.8) 0%, rgba(226,130,178, 1) 100%);
            display: flex;
        }

        &__overlay {
            @include dflex(space-between);
            flex-direction: column;
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            padding: 1.25rem;
            display: none;
            color: var(--primary-color-text);

            &-info {
                @include dflex(center);
                flex-direction: column;
                text-align: center;
                flex-grow: 1;
            }

            &-button {
                @include dflex(space-between);
            }
        }

        &__category {
            margin: .625rem 0;
        }

        &__category,
        &__price {
            display: block;
        }

        &__category,
        &__cart,
        &__details {
            font-size: .75rem;
        }

        &__cart {
            margin-right: 1.5rem;
        }

        &__cart,
        &__details {
            cursor: pointer;
        }
    }

</style>