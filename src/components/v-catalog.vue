<template>
    <div class="v-catalog">
        <h2>Catalog</h2>
        <div class="v-catalog-container">
            <v-catalog-item 
                v-for="product in products"
                :key="product.article"
                :product_data="product"
            />
        </div>
    </div>
</template>

<script>
    import vCatalogItem from './v-catalog-item';


    export default {
        name: 'v-catalog',
        components: {
            vCatalogItem
        },
        props: {},
        data() {
            return {
                  products: [
                        {
                            image: "1.jpg",
                            name: "T-shirt 1",
                            price: 2100.2,
                            article: "T1",
                            available: true,
                            category: "Мужские"
                        },
                        {
                            image: "1.jpg",
                            name: "T-shirt 44",
                            price: 100.23423,
                            article: "T12",
                            available: false,
                            category: "Мужские"
                        },
                        {
                            image: "1.jpg",
                            name: "Some",
                            price: 300,
                            article: "T13",
                            available: true,
                            category: "Мужские"
                        },
                        {
                            image: "1.jpg",
                            name: "Ben sherman",
                            price: 3500,
                            article: "T14",
                            available: true,
                            category: "Мужские"
                        },
                        {
                            image: "1.jpg",
                            name: "Lacoste",
                            price: 7000,
                            article: "T15",
                            available: false,
                            category: "Мужские"
                        },
                        {
                            image: "1.jpg",
                            name: "Fred Perry",
                            price: 500,
                            article: "T16",
                            available: true,
                            category: "Мужские"
                        },
                    ]
            }
        }
    }
</script>

<style lang="scss" scoped>
    .v-catalog {
        width: 100%;
        border: 1px solid;
        &-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: flex-start;
            padding: 0 15px;
            max-width: 1170px;
            margin: 0 auto;
        }
    }
</style>