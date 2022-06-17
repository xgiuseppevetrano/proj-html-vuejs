<template>
    <nav class="nav-bar">
        <ul class="nav-bar__list">
            <li class="nav-bar__item" :class="{active: link.isActive, 'border': link.isBorder}" v-for="(link, index) in links" :key="index">
                <span v-show="link.icon"><i :class="link.icon"></i></span>
                <a class="nav-bar__item-link" href="#">{{link.text}}</a>
                <span v-show="link.isDropDown" class="nav-bar__item-icon"><i class="fa-solid fa-chevron-down"></i></span>
            </li>
        </ul>
    </nav>
</template>

<script>
    export default {
        name: 'BaseNav',
        props: {
            links: Array
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
            font-size: .875rem;
            padding: .9375rem;

            &.active {
                color: var(--secondary-color-text);
                padding: .9375rem 3.75rem;
                background-color: var(--quinary-bg-color);
            }

            &.active .nav-bar__item-link{
                color: var(--secondary-color-text);
                text-transform: uppercase;
                font-weight: 500;
            }

            &.active .nav-bar__item-icon{
                font-size: .875rem;
            }

            &.border {
                border-right: 1px solid var(--quinary-color-text);
                border-left: 1px solid var(--quinary-color-text);
            }

            &-link {
                text-decoration: none;
                color: var(--tertiary-color-text);
                margin: 0 .625rem;
            }

            &-icon {
                font-size: .75rem;
            }
        }
    }
</style>