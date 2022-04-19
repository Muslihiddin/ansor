<template>
    <div class="recognizedBrands py-20 md:py-32">
        <div class="container xl:max-w-7xl mx-auto px-2.5 pb-5 sm:px-0">
            <div class="text flex flex-col md:flex-row md:gap-x-5 items-center justify-between">
                <h1 class="md:max-w-2xl w-full pb-5 md:pb-0">We are trusted technology partner for <span>recognized brands</span></h1>
                <p class="pageDescription lg:max-w-lg md:max-w-sm ">We give you exact quote before starting your project, and we stick to it!
                We give you exact quote before starting your project, and we stick to it!
                </p>
            </div>
            <brands />
        </div>
    </div>
</template>

<script>
import Brands from './Brands.vue'
export default {
  components: { Brands },
    name: 'RecognizedBrandsBlock'
}
</script>

<style lang="scss" scoped>
    span {
        color: #3DB079;
    }
</style>