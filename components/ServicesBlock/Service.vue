<template>
    <div class="service py-7 px-8 max-w-xs sm:max-w-md">
            <icon :name="item.icon" />
            <h3 class="text-2xl leading-8 font-bold mt-3 mb-2">{{ item.title }}</h3>
            <p class="text-sm leading-6">{{ item.description }}</p>
        </div>
</template>

<script>
import Icon from '../../assets/Shared/Icon.vue'
    export default {
        components: { Icon },
        name: 'ServiceCard',
        props: ['item']
    }
</script>

<style lang="scss" scoped>
    h3{
        color: var(--Green_01);
        font-family: var(--rubik);
    }

    p{
        font-family: var(--montserrat);
        color: var(--Black_03);
    }

</style>