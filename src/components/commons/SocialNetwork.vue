<template>
    <div class="social">
        <i class="social__icon" v-for="(social, index) in socials" :key="index" :class="`fa-brands ${social}`"></i>
    </div>
</template>

<script>
    export default {
        name: 'SocialNetwork',
        data() {
            return {
                socials: [
                    'fa-facebook-f',
                    'fa-twitter',
                    'fa-instagram',
                    'fa-youtube'
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
    .social {
        color: var(--primary-color-social);
        padding: .625rem 0;

        &__icon {
            margin-right: 1.25rem;
        }
    }
</style>