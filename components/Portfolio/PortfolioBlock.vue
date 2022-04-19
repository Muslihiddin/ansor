<template>
    <div class="portfolio" id="portfolio">
        <div class="container xl:max-w-7xl mx-auto px-2.5 pb-5 sm:px-0">
            <div class="text text-center">
                <h1>Our portfolio</h1>
                <p class="pageDescription">We give you exact quote before starting your project, and we stick to it!</p>
            </div>
            <portfolio-brands />
        </div>
    </div>
</template>

<script>
import PortfolioBrands from './PortfolioBrands.vue'
export default {
  components: { PortfolioBrands },

}
</script>

<style>

</style>