<template>
    <div class="footer-bottom">
        <div class="container">
            <small class="footer-bottom__text">
                <i class="fa-regular fa-copyright"></i> Copyright 2012 - 2020  |  
                Avada Theme by Theme Fusion  |  
                All Rights Reserved  |  
                Powered by WordPress
            </small>
            <img class="footer-bottom__img" src="../../assets/img/payment_cards_footer.png" alt="payment cards">
        </div>
    </div>
</template>

<script>
    export default {
        name: 'FooterBottom',
    }
</script>

<style lang="scss" scoped>
    .footer-bottom {
        background-color: var(--quaternary-bg-color);
        padding: 1.875rem 0;
        text-align: center;

        &__text {
            color: var(--quinary-color-text);
            display: block;
            margin-bottom: 1.25rem;
        }
    }
</style>