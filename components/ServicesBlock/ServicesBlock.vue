<template>
    <div id="services" class="servicesBlock xl:py-28 lg:py-20 md:py-16 sm:py-12 sm:py-11 py-10">
        <div class="container xl:max-w-7xl mx-auto px-2.5 sm:px-0">
            <h1 class="xl:mb-12 mb-8">Our services</h1>
            <services-list />
        </div>
    </div>
</template>

<script>
import ServicesList from './ServicesList.vue'
export default {
  components: { ServicesList },
    name: 'ServicesBlock'
}
</script>

<style>

</style>