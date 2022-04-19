<template>
    <div class="flex items-center justify-center">
        <div class="teamVideo">
            <a href="https://youtu.be/dQw4w9WgXcQ" target="blank">
                <img src="../../assets/images/playButton.png" alt="">
            </a>
            <a href="https://youtu.be/dQw4w9WgXcQ" target="blank" class="pointer">
                <img src="../../assets/images/teamVideo.png" alt="">
            </a>
        </div>
    </div>
</template>
<style lang="scss" scoped>
    .pointer {
        position: relative;
        top: -55px;
        left: 95px;
    }

    @media screen and(max-width: 600px) {
        .flex {
            position: relative;
        }
        .teamVideo {
            position: absolute;
            bottom: -147px;
            right: 115px;
            transform: rotate(-15deg);
        }
    }
</style>
