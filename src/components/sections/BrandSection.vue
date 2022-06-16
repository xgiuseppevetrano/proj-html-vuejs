<template>
    <section class="brand">
        <div class="container">
            <h5 class="brand__title">Brand Logos</h5>
            <div class="brand__box">
                <img v-for="(image, i) in images" :key="i" :src="require(`../../assets/img/${image}`)">
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        name: 'BrandSection',
        data() {
            return {
                images: [
                    'b_logotype_6.png',
                    'b_logotype_7.png',
                    'b_logotype_1.png',
                    'b_logotype_2.png',
                    'b_logotype_3.png'
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
    @import '../../assets/style/mixins.scss';

    .brand {
        margin: 2.5rem 0 0;
        background-color: var(--quinary-bg-color);
        padding: 2.5rem;
        text-align: center;

        &__title {
            text-transform: uppercase;
            color: var(--septenary-color-text);
            font-weight: 500;
        }

        &__box {
            margin-top: 1.875rem;
            @include dflex(space-around);
        }
    }
</style>