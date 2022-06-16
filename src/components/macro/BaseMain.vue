<template>
    <main>
        <HeroSection/>
        <FeaturedProductsSection/>
        <CollectionSection/>
        <BestSellerSection/>
        <PromoSection/>
    </main>
</template>

<script>
    import HeroSection from "../sections/HeroSection.vue";
    import FeaturedProductsSection from "../sections/FeaturedProductsSection.vue";
    import CollectionSection from '../sections/CollectionSection.vue';
    import BestSellerSection from '../sections/BestSellerSection.vue';
    import PromoSection from '../sections/PromoSection.vue';

    export default {
        name: 'BaseMain',
        components: {
            HeroSection,
            FeaturedProductsSection,
            CollectionSection,
            BestSellerSection,
            PromoSection,
        }
    }
</script>

<style lang="scss" scoped>

</style>