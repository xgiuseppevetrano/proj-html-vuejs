<template>
    <div>
        <img class="card__img" :src="require(`../../assets/img/${card.src}`)" :alt="card.title">
        <div class="card__overlay">
            <h2 class="card__title">{{card.title}}</h2>
            <small class="card__description">{{card.description}}</small>
            <small v-show="card.descriptionPlus" class="card__description-plus">{{card.descriptionPlus}}</small>
            <div>
                <BaseButton class="button__item button__transparent button__small" :text="card.button"/>
            </div>
        </div>
    </div>
</template>

<script>
    import BaseButton from './BaseButton.vue'

    export default {
        name: 'BigCard',
        components: {
            BaseButton
        },
        props: {
            card: Object
        },
    }
</script>

<style lang="scss" scoped>
    .card {
        color: var(--primary-color-text);
        position: relative;

        &--big {
            text-align: center;
            
            .card__img {
                height: 30.375rem;
                object-fit: cover;
            }

            .card__description {
                display: inline-block;
                margin: .9375rem 0;
            }

            .card__overlay {
                padding: 1.25rem;
            }
        }

        &--rectangular {
            .card__img {
                height: 15.625rem;
                object-fit: contain;
            }

            .card__title {
                margin-bottom: .625rem;
            }

            .card__description {
                display: block;
            }

            .card__description,
            .card__description-plus {
                font-size: 12px;
            }

            .button__item {
                margin-top: .9375rem;
            }

            .card__overlay {
                padding: 1.25rem 2.5rem;
            }
        }

        &__img {
            object-position: top;
        }

        &__overlay {
            position: absolute;
            bottom: 2.5rem;
            left: 0;
            right: 0;
        }
    }
</style>