<template>
    <main>
        <HeroSection/>
        <FeaturedProductsSection/>
        <CollectionSection/>
        <BestSellerSection/>
        <PromoSection/>
        <NewArrivalsSection/>
        <TestimonialSection/>
        <BlogSection/>
        <div class="line"></div>
        <ProductsSection/>
        <BrandSection/>
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
    import BlogSection from '../sections/BlogSection.vue';
    import ProductsSection from '../sections/ProductsSection.vue';
    import BrandSection from '../sections/BrandSection.vue';

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
            BlogSection,
            ProductsSection,
            BrandSection
        }
    }
</script>

<style lang="scss" scoped>
    main {

        .line {
            margin: auto;
            width: 97%;
            height: .0625rem;
            background-color: var(--primary-bg-color);
        }
    }
</style>
