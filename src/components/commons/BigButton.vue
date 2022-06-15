<template>
    <div class="button">
        <button class="button__item">{{text}}</button>
    </div>
</template>

<script>
    export default {
        name: 'BigButton',
        props: {
            text: String
        }
    }
</script>

<style lang="scss" scoped>
    .button {
        &__item {
            text-transform: uppercase;
            background-color: rgba(255,255,255,0.2);
            padding: .75rem 1.875rem;
            color: var(--primary-color-text);
            border: 1px solid var(--primary-color-text);
            border-radius: 1.25rem;
            font-weight: 600;
            margin-right: .9375rem;
        }
    }
</style>