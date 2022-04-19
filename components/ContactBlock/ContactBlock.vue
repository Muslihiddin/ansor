<template>
  <div class="contactBlock my-20 md:my-32" id="contact_us">
      <div class="container xl:max-w-7xl mx-auto px-2.5 pb-5 sm:px-0">
        <div class="wrapper flex flex-col lg:flex-row md:gap-x-32 items-center justify-between">      
            <div class="title flex flex-col items-center lg:block">
                <icon name="biglogo" />
                <h1>Contact Us</h1>
                <p class="pageDescription max-w-lg lg:max-w-none">We give you exact quote before starting your project, and we stick to it!</p>
                <icon name="fancyArrow" class="fancyBoi" />
            </div>
            <contact-form />
        </div>
      </div>
  </div>
</template>

<script>
import Icon from '../../assets/Shared/Icon.vue'
import ContactForm from './ContactForm.vue'
export default {
  components: { Icon, ContactForm },
}
</script>

<style lang="scss" scoped>
    .title  {
        position: relative;
    }

    .fancyBoi {
        position: absolute;
        bottom: 40%;
        right: -30px;
    }

@media screen and(max-width: 1280px) {
    .fancyBoi {
        display: none;
    }
}
</style>