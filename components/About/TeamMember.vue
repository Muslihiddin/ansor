<template>
    <div class="teamMember">
        <img :src="require('../../assets/images/' + member.img)"  alt="">
        <h2 class="mt-4 mb-1 font-semibold text-2xl leading-7">{{ member.name }}</h2>
        <p class="text-2xl font-light leading-7">{{ member.position }}</p>
    </div>
</template>

<script>
export default {
    name: 'TeamMember',
    props: ['member']
}
</script>

<style lang="scss" scoped>
    h2 {
        font-family: var(--rubik);
        color: #3db079;
    }

    p {
        font-family: var(--rubik);
        color: #B4B4B4;
    }

    img {
        max-width: 268px;
    }
</style>
