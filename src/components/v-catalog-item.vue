<template>
    <div class="v-catalog-item">
        <div class="title">{{product_data.name}}</div>
        <div class="img">
            <img src="https://theroco.com/assets/2017/12/xiaomi-redmi-4x-review-1.jpg" alt="">
        </div>
        <div class="stock">
            {{product_data.available ? 'In Stock' : 'Not in stock'}}
        </div>
        <div class="price">
            Price:
            <div class="price-value">
                {{product_data.price}}
                <span class="currency">$</span>
            </div>
        </div>
        <button class="atc-button">Add to cart</button>
    </div>
</template>

<script>
    export default {
        name: 'v-catalog-item',
        props: {
            product_data: {
                type: Object,
                default() {
                    return {}
                }
            }
        },
        data() {
            return {}
        }
    }
</script>

<style lang="scss" scoped>
    .v-catalog-item {
        box-shadow: 0 0 5px rgba(0,0,0,0.4);
        padding: 10px;
        min-height: 200px;
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        flex: 0 0 190px;
        max-width: 190px;
        margin: 10px;

        .title {
            width: 100%;
            text-overflow: ellipsis;
            white-space: nowrap;
            overflow: hidden;

        }

        .img {
            border: 1px solid;
            height: 100px;
            display: flex;
            justify-content: center;
            align-items: center;

            img {
                max-width: 100%;
                width: auto;
                max-height: 100%;
                height: auto;
                margin: 0 auto;
            }
        }
    }
</style>