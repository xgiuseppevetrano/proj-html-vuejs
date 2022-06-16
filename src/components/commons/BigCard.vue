<template>
    <div class="card" :style="{backgroundImage: `url(${require('@/assets/img/' + card.src)})`}">
        <h3 class="card__title">{{card.title}}</h3>
        <small class="card__description">{{card.description}}</small>
        <div>
            <BaseButton class="card__button" :text="card.button"/>
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
        padding: 3.125rem;
        background-size: cover;
        text-align: center;
    }
</style>