<template>
    <footer>
        <FooterTop/>
        <FooterCenter/>
        <FooterBottom/>
    </footer>
</template>

<script>
    import FooterBottom from '../sections/FooterBottom.vue'
    import FooterCenter from '../sections/FooterCenter.vue'
    import FooterTop from '../sections/FooterTop.vue'
    
    export default {
        name: 'BaseFooter',
        components: {
            FooterTop,
            FooterCenter,
            FooterBottom
        }
    }
</script>

<style lang="scss" scoped>

</style>