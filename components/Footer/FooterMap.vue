<template>
    <div class="map">
        <iframe class="actual-map" width="100%" height="600" frameborder="16px" scrolling="no" src="https://maps.google.com/maps?width=100%25&amp;height=600&amp;hl=en&amp;q=43%20Chapanata%20ko'chasi,%20%D0%A2%D0%B0%D1%88%D0%BA%D0%B5%D0%BD%D1%82+(My%20Business%20Name)&amp;t=&amp;z=15&amp;ie=UTF8&amp;iwloc=B&amp;output=embed">
        <a href="https://www.gps.ie/marine-gps/">shipping gps</a>
        </iframe>
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
    .map {
        width: 100%;
        border-radius: 16px;
        margin-top: 36px;
        .actual-map {
            border-radius: 16px;
            width: 100%;
            max-height: 275px;
        }
    }
</style>