<template>
    <button>{{text}}</button>
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
            padding: .625rem 1.25rem;
            color: var(--primary-color-text);
            border-radius: 1.25rem;
            font-weight: 600;
            margin-right: 2.1875rem;
        }

        &__blue {
            background-color: var(--bg-color-button);
            border: none;

        }

        &__transparent {
            background-color: rgba(255,255,255,0.2);
            border: 1px solid var(--primary-color-text);
        }

        &__big {
            padding: .75rem 1.875rem;
            margin-right: .9375rem;
        }

        &__small {
            padding: .5rem .75rem;
            font-size: .75rem;
            margin-right: 0;
        }
    }
</style>