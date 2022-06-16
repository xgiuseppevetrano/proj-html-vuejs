<template>
    <main>
        <HeroSection/>
        <FeaturedProductsSection/>
        <CollectionSection/>
        <BestSellerSection/>
    </main>
</template>

<script>
    import HeroSection from "../sections/HeroSection.vue";
    import FeaturedProductsSection from "../sections/FeaturedProductsSection.vue";
    import CollectionSection from '../sections/CollectionSection.vue';
    import BestSellerSection from '../sections/BestSellerSection.vue';

    export default {
        name: 'BaseMain',
        components: {
            HeroSection,
            FeaturedProductsSection,
            CollectionSection,
            BestSellerSection
        }
    }
</script>

<style lang="scss" scoped>

</style>