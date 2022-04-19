<template>
    <div class="brands mt-14 md:mt-20">
            <icon name='walmart' />
            <icon name='microsoft' />
            <icon name='hubspot' />
            <icon name='airbnb' />
            <icon name='walmart' />
            <icon name='hubspot' />
            <icon name='walmart' />
            <icon name='microsoft' />
            <icon name='hubspot' />
            <icon name='airbnb' />
            <icon name='walmart' />
    </div>
</template>

<script>
import Icon from '../../assets/Shared/Icon.vue'
export default {
  components: { Icon },

}
</script>

<style lang="scss" scoped>
    .brands {
        display: grid;
        justify-items: center;
        grid-template-columns: repeat( auto-fit, minmax(190px, 1fr) );
        grid-column-gap: 95px;
        grid-row-gap: 40px;
    }
    
</style>