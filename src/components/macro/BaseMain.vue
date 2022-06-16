<template>
    <main>
        <HeroSection/>
        <FeaturedProductsSection/>
        <CollectionSection/>
        <BestSellerSection/>
        <PromoSection/>
        <NewArrivalsSection/>
        <TestimonialSection/>
    </main>
</template>

<script>
    import HeroSection from "../sections/HeroSection.vue";
    import FeaturedProductsSection from "../sections/FeaturedProductsSection.vue";
    import CollectionSection from '../sections/CollectionSection.vue';
    import BestSellerSection from '../sections/BestSellerSection.vue';
    import PromoSection from '../sections/PromoSection.vue';
    import NewArrivalsSection from '../sections/NewArrivalsSection.vue';
    import TestimonialSection from '../sections/TestimonialSection.vue';

    export default {
        name: 'BaseMain',
        components: {
            HeroSection,
            FeaturedProductsSection,
            CollectionSection,
            BestSellerSection,
            PromoSection,
            NewArrivalsSection,
            TestimonialSection,
        }
    }
</script>