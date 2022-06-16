<template>
    <div class="card">
        <img class="card__img" :src="require(`../../assets/img/${card.src}`)" :alt="card.title">
        <div class="card__overlay">
            <h2 class="card__title">{{card.title}}</h2>
            <small class="card__description">{{card.description}}</small>
            <div>
                <BaseButton class="button__item button__transparent button__small" :text="card.button"/>
            </div>
        </div>
    </div>
</template>

<script>
    import BaseButton from './BaseButton.vue'

    export default {
        name: 'BigCard',
        components: {
            BaseButton
        },
        props: {
            card: Object
        },
    }
</script>

<style lang="scss" scoped>
    .card {
        background-size: cover;
        text-align: center;
        color: var(--primary-color-text);
        position: relative;

        &__img {
            width: 100%;
            height: 30.375rem;
            object-fit: cover;
            object-position: top;
        }

        &__overlay {
            position: absolute;
            bottom: 2.5rem;
            left: 0;
            right: 0;
            padding: 1.25rem;
        }

        &__description {
            display: inline-block;
            margin: .9375rem 0;
        }
    }
</style>