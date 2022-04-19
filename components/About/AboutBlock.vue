<template>
    <div class="about" id="about">
        <div class="container xl:max-w-7xl mx-auto px-2.5 pb-20 sm:px-0">
            <div class="aboutPageTitle max-w-3xl mx-auto text-center">
                <h1>About Our Team</h1>
                <p class="pageDescription">We are a very experienced web &#38; mobile app development team We are a very experienced web &#38; mobile app development team</p>
            </div>
            <team-list />
            <team-video />
        </div>
    </div>
</template>

<script>
import TeamList from './TeamList.vue'
import TeamVideo from './TeamVideo.vue'
export default {
    name: 'AboutBlock',
    components: {
        TeamList,
        TeamVideo
    }
}
</script>

