<template>
    <div class="card">
        <img class="card__img" :src="require(`../../assets/img/${card.src}`)" :alt="card.title">
        <h5 class="card__title">{{card.title}}</h5>
        <small class="card__info">{{card.info}}</small>
        <p class="card__text">{{card.text}}</p>
    </div>
</template>

<script>
    export default {
        name: 'BlogCard',
        props: {
            card: Object
        }
    }
</script>

<style lang="scss" scoped>
    .card {
        &__img {
            width: 100%;
        }

        &__title {
            color: var(--secondary-color-text);
            margin-top: .625rem;
        }

        &__info,
        &__text {
            color: var(--tertiary-color-text);
        }

        &__info {
            font-size: .75rem;
            margin: .5rem 0 .75rem;
            display: inline-block;
        }

        &__text {
            font-size: .875rem;
            line-height: 1.375rem;
        }
    }
</style>