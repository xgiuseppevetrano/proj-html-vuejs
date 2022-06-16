<template>
    <section class="promo">
        <div class="container">
            <div class="promo__cards">
                <BigCard class="card card--rectangular" v-for="(card, i) in cards" :key="i" :card="card"/>
            </div>
        </div>
    </section>
</template>

<script>
import BigCard from '../commons/BigCard.vue'
    export default {
        name: 'PromoSection',
        components: {
            BigCard
        },
        data() {
            return {
                cards: [
                    {
                        src: 'promo_box_1_bg.jpg',
                        title: '70% Off',
                        description: 'Vivamus tempor leo lacus, feugiat',
                        descriptionPlus: 'ut magna aliquam erat',
                        button: 'View more'
                    },
                    {
                        src: 'promo_box_2_bg.jpg',
                        title: 'Free Shipping',
                        description: 'Vivamus tempor leo lacus, feugiat',
                        descriptionPlus: 'ut magna aliquam erat',
                        button: 'View more'
                    }
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
    @import '../../assets/style/mixins.scss';

    .promo {
        background-image: url('http://localhost:8080/img/bkgd_confetti-compressor.ae1799af.jpg');
        background-position: center;
        background-size: cover;
        background-repeat: no-repeat;
        padding: 4.375rem 0;

        &__cards {
            @include dflex(center);

            .card {
                margin: 30px;
            }
        }
    }
</style>