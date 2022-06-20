<template>
    <div class="tag">
        <small>{{tag}}</small>
    </div>
</template>

<script>
    export default {
        name: 'BaseTags',
        props: {
            tag: String
        }
    }
</script>

<style lang="scss" scoped>
    .tag {
        border: 1px solid var(--senary-color-text);
        padding: .3125rem;
        display: inline-block;
        margin: .1875rem;
    }
</style>