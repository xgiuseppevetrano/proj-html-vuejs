<template>
    <div>
        <div class="container">
            <SocialNetwork/>
        </div>
    </div>
</template>

<script>
    import SocialNetwork from "../commons/SocialNetwork.vue";

    export default {
        name: 'HeaderTop',
        components: {
            SocialNetwork
        }
    }
</script>

<style lang="scss" scoped>

</style>