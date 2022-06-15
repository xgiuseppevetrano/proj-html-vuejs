<template>
    <div class="card" :style="{backgroundImage: `url(${require('@/assets/img/' + card.src)})`}">
        <h3>{{card.title}}</h3>
        <small>{{card.description}}</small>
        <button>{{card.button}}</button>
    </div>
</template>

<script>
    export default {
        name: 'BigCard',
        props: {
            card: Object
        },
    }
</script>

<style lang="scss" scoped>
    .card {
        padding: 3.125rem;
        background-size: cover;
    }
</style>