<template>
    <div class="title">
        <div class="title__top">
            <div class="title__top-line"></div>
            <h2 class="title__top-text">{{title}}</h2>
            <div class="title__top-line"></div>
        </div>
        <small class="title__bottom">{{text}}</small>
    </div>
</template>

<script>
    export default {
        name: 'BaseTitle',
        props: {
            title: String,
            text: String
        }
    }
</script>

<style lang="scss" scoped>
    @import '../../assets/style/mixins.scss';

    .title {
        text-align: center;

        &__top {
            @include dflex(center);

            &-line {
                width: 32%;
                height: .05rem;
                background-color: var(--quinary-color-text);
            }

            &-text {
                margin: 0 2.1875rem;
                font-size: 2rem;
                color: var(--secondary-color-text);
            }
        }

        &__bottom {
            color: var(--tertiary-color-text);
        }
    }
</style>