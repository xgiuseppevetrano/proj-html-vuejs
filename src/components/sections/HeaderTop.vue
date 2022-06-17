<template>
    <div>
        <div class="container">
            <div class="header-top">
                <SocialNetwork/>
                <SmallNav :links="links"/>
            </div>
        </div>
    </div>
</template>

<script>
    import SocialNetwork from "../commons/SocialNetwork.vue";
    import SmallNav from "../commons/SmallNav.vue";

    export default {
        name: 'HeaderTop',
        components: {
            SocialNetwork,
            SmallNav
        },
        data() {
            return {
                links: [
                    {
                        text: 'Shipping Cart',
                        isActive: false,
                        isDropDown: false,
                        isBorder: false,
                    },
                    {
                        text: 'My Account',
                        isActive: false,
                        isDropDown: true,
                        isBorder: true,
                    },
                    {
                        text: 'Cart',
                        isActive: true,
                        isDropDown: true,
                        isBorder: false,
                        icon: 'fa-solid fa-cart-shopping'
                    },

                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
    @import '../../assets/style/mixins.scss';

    .header-top {
        @include dflex(space-between);
    }
</style>