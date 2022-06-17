<template>
    <div class="footer-top">
        <div class="container">
            <div class="footer-top__box">
                <div class="footer-top__text">
                    <span class="footer-top__icon"><i class="fa-regular fa-envelope"></i></span>
                    <h3 class="footer-top__title">Subscribe now and get special offers</h3>
                </div>
                <form class="footer-top__form">
                    <input class="footer-top__input" type="text" placeholder="Insert your email">
                    <BaseButton class="button__item button__blue button__long" text="Send"/>
                </form>
            </div>
        </div>
    </div>
</template>

<script>
    import BaseButton from "../commons/BaseButton.vue";

    export default {
        name: 'FooterTop',
        components: {
            BaseButton
        }
    }
</script>

<style lang="scss" scoped>
    @import '../../assets/style/mixins.scss';

    .footer-top {
        background-color: var(--secondary-bg-color);
        padding: 2.5rem 0;

        &__box {
            @include dflex(space-between);
        }

        &__text {
            @include dflex(space-around); 
        }

        &__icon {
            color: var(--tertiary-color-text);
            padding: .5rem .625rem;
            background-color: var(--tertiary-bg-color);
            border-radius: 50%;
            margin-right: 1.25rem;
            font-size: 22px;
        }
        
        &__title {
            color: var(--primary-color-text);
        }
        
        &__input {
            color: var(--quinary-color-text);
            padding: .375rem .5rem;
            border-radius: 1.25rem;
            border: none;
            margin-right: .625rem;
        }
    }
</style>