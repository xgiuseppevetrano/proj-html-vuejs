<template>
    <nav class="nav-bar">
        <ul class="nav-bar__list">
            <li class="nav-bar__item" :class="{active : link.isActive}" v-for="(link, index) in links" :key="index">
                <a class="nav-bar__item-link" href="#">{{link.text}}</a>
                <span v-show="link.isDropDown" class="nav-bar__item-icon"><i class="fa-solid fa-chevron-down"></i></span>
                <div v-show="link.isActive" class="nav-bar__item-line"></div>
            </li>
        </ul>
    </nav>
</template>

<script>
    export default {
        name: 'BaseNav',
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

    .nav-bar {
        &__list {
            @include dflex(space-between);
        }

        &__item {
            list-style-type: none;
            color: var(--tertiary-color-text);
            margin-right: 2.1875rem;
            font-size: .875rem;
            position: relative;

            &.active {
                color: var(--color-active-link);
            }

            &.active .nav-bar__item-link{
                color: var(--color-active-link);
            }

            &-link {
                text-decoration: none;
                color: var(--tertiary-color-text);
                margin-right: .625rem;
            }

            &-icon {
                font-size: .75rem;
            }

            &-line {
                position: absolute;
                top: -2.875rem;
                right: 0;
                width: 3.9375rem;
                height: .125rem;
                background-color: var(--color-active-link);
            }
        }

    }
</style>