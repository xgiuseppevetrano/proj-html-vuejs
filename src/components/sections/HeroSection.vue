<template>
    <section class="hero">
        <div class="container">
            <div class="hero__info">
                <h1 class="hero__info-title">Brand New Arrivals</h1>
                <span class="hero__info-text">New collection from New York</span>
                <div class="hero__info-button">
                    <BaseButton class="button__item button__transparent button__big" text="View all"/>
                    <BaseButton class="button__item button__transparent button__big" text="Lookbook"/>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    import BaseButton from '../commons/BaseButton.vue'

    export default {
        name: 'HeroSection',
        components: {
            BaseButton
        }
    }
</script>

<style lang="scss" scoped>
    @import '../../assets/style/mixins.scss';

    .hero {
        background-image: url("../../assets/img/home1_slide_three_bg_2.jpg");
        background-position-y: center;
        background-size: cover;
        background-repeat: no-repeat;
        height: 32.5rem;
        @include dflex(center);

        &__info {
            display: flex;
            flex-direction: column;
            align-items: center;
            color: var(--primary-color-text);

            &-title {
                font-size: 3.75rem;
            }

            &-text {
                margin: .625rem 0 1.875rem;
                font-size: 1.25rem;
                text-transform: uppercase;
            }

            &-button {
                @include dflex(center);
            }
        }

    }
</style>