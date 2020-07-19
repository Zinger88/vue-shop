<template>
    <div class="v-main-wrapper">
        <v-catalog></v-catalog>
        <v-cart></v-cart>
    </div>
</template>

<script>
    import vCatalog from './v-catalog';
    import vCart from './v-cart';

    export default {
        name: 'v-main-wrapper',
        components: {
            vCatalog,
            vCart
        },
        props: {},
        data() {
            return {
                title: 'Main Wrapper'
            }
        },
        computed: {},
        methods: {},
        watch: {},
        mounted() {
            console.log('mounted')
        }
     }
</script>

<style scoped lang="scss">
    .v-main-wrapper {
        display: flex;
        justify-content: center;
        flex-direction: column;
        align-items: center;
        margin: 0 auto;
    }
</style>

