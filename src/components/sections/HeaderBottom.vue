<template>
    <div>
        <div class="container">
            <div class="header-bottom">
                <BaseLogo/>
                <div class="header-bottom__elements">
                    <BaseNav :links="links"/>
                    <BaseButton class="button__item button__blue" text="Shop Now!"/>
                    <span class="icon"><i class="fa-solid fa-magnifying-glass"></i></span>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import BaseLogo from '../commons/BaseLogo.vue';
    import BaseNav from '../commons/BaseNav.vue';
    import BaseButton from '../commons/BaseButton.vue';

    export default {
        name: 'HeaderBottom',
        components: {
            BaseLogo,
            BaseNav,
            BaseButton
        },
        data() {
            return {
                links: [
                    {
                        text: 'Home',
                        isActive: true,
                        isDropDown: true
                    },
                    {
                        text: 'Shop',
                        isActive: false,
                        isDropDown: true

                    },
                    {
                        text: 'Products',
                        isActive: false,
                        isDropDown: true
                    },
                    {
                        text: 'Categories',
                        isActive: false,
                        isDropDown: true
                    },
                    {
                        text: 'News',
                        isActive: false,
                        isDropDown: false
                    },
                    {
                        text: 'Elements',
                        isActive: false,
                        isDropDown: true
                    },
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
    @import '../../assets/style/mixins.scss';

    .header-bottom {
        @include dflex(space-between);
        padding: 1.875rem 0;

        &__elements {
            @include dflex(space-between);

        }

        .icon {
            color: var(--tertiary-color-text);
        }
    }
</style>