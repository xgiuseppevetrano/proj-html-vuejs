<template>
    <main>
        <HeroSection/>
        <FeaturedProductsSection/>
    </main>
</template>

<script>
    import HeroSection from "../sections/HeroSection.vue";
    import FeaturedProductsSection from "../sections/FeaturedProductsSection.vue";

    export default {
        name: 'BaseMain',
        components: {
            HeroSection,
            FeaturedProductsSection,
        }
    }
</script>

<style lang="scss" scoped>

</style>