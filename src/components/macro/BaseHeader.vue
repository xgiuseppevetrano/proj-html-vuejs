<template>
    <header>
        <HeaderTop class="header-top"/>
        <HeaderBottom/>
    </header>
</template>

<script>
    import HeaderTop from "../sections/HeaderTop.vue";
    import HeaderBottom from "../sections/HeaderBottom.vue";

    export default {
        name: 'BaseHeader',
        components: {
            HeaderTop,
            HeaderBottom
        }
    }
</script>

<style lang="scss" scoped>
    .header-top {
        border-bottom: 1px solid var(--quinary-color-text);
    }
</style>