<template>
    <div class="post">
        <small><i class="post__icon fa-solid fa-angle-right"></i>{{post}}</small>
    </div>
</template>

<script>
    export default {
        name: 'BasePosts',
        props: {
            post: String
        }
    }
</script>

<style lang="scss" scoped>
    .post {
        display: inline-block;
        border-bottom: 1px solid var(--senary-color-text);
        padding: .9375rem 0;
        display: flex;

        &__icon {
            margin-right: .625rem;
        }
    }
</style>