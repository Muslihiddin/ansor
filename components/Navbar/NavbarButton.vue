<template>
    <a href="#contact_us">Contact Us</a>
</template>

<script>
export default {
    name: 'NavbarButton'
}
</script>

<style lang="scss" scoped>
    a {
        font-family: var(--montserrat);
        font-weight: 600;
        font-size: 16px;
        line-height: 24px;
        color: #fff;

        border: none;
        padding: 16px 57px;
        margin-left: 96px;
        background-color: var(--Green_01);
        border-radius: 8px;

        &:active {
            transform: scale(0.99);
        }
        &:hover {
            box-shadow: 0 5px 30px var(--Green_01)
        }
    }

</style>