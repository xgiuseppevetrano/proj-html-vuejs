<template>
    <div class="button">
        <button class="button__item">{{text}}</button>
    </div>
</template>

<script>
    export default {
        name: 'BaseButton',
        props: {
            text: String
        }
    }
</script>

<style lang="scss" scoped>
    .button {
        &__item {
            text-transform: uppercase;
            background-color: var(--bg-color-button);
            padding: .625rem 1.25rem;
            color: var(--primary-color-text);
            border: none;
            border-radius: 1.25rem;
            font-weight: 600;
            margin-right: 2.1875rem;
        }
    }
</style>