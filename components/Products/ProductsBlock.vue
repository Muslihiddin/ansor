<template>
    <div class="productsBlock pt-20 pb-28">
        <div class="container xl:max-w-7xl mx-auto px-2.5 pb-5 sm:px-0">
            <h1 class="text-center text-white">We create digital products</h1>
            <p class="pageDescription text-center max-w-3xl mx-auto">We are a very experienced web &#38; mobile app development team We are a very experienced web &#38; mobile app development team</p>
            <products-numbers />
        </div>
    </div>
</template>

<script>
import ProductsNumbers from './ProductsNumbers.vue'
export default {
    name: 'productsBlock',
    components: {
        ProductsNumbers
    }
}
</script>

<style lang='scss' scoped>
    .productsBlock {
        background-color: #163828;
    }

    @media screen and(max-width: 500px) {
        h1 {
            line-height: 50px;
            margin-bottom: 15px;
        }
    }

</style>