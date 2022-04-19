<template>
    <div class="footer pt-28 pb-20" id="contact">
        <div class="container xl:max-w-7xl mx-auto px-2.5 pb-5 sm:px-0">
            <div class="contact-links pb-8 flex justify-between">
                <h1 class="text-white">Contacts</h1>
                <ul class="text-white">
                    <li class="flex flex-col lg:w-auto lg:ml-20"><span class="text-base font-semibold leading-8 opacity-60 pb-0.5">E-mail</span>
                        <a href="mailto:ansor@info.com" class="text-2xl font-semibold">Ansor@info.com</a>
                    </li>
                    <li class="flex flex-col lg:w-auto lg:ml-20"><span class="text-base font-semibold leading-8 opacity-60 pb-0.5">Phone number</span>
                        <a href="tel:+998911529721" class="text-2xl font-semibold">+998 91 152 97 21</a>
                    </li>
                    <li class="flex flex-col lg:w-auto lg:ml-20"><span class="text-base font-semibold leading-8 opacity-60 pb-0.5">E-mail</span>
                        <a href="telegram.me/@ansor.io" class="text-2xl font-semibold">@ansor.io</a>
                    </li>
                    <li class="flex flex-col lg:ml-20"><span class="text-base font-semibold leading-8 opacity-60 pb-0.5">Social media</span>
                      <div class="social-icons">
                        <a href="mailto:ansor@info.com"><social-media-icons name='instagram' class="instagram" /></a>
                        <a href="mailto:ansor@info.com"><social-media-icons name='telegram' /></a>
                        <a href="mailto:ansor@info.com"><social-media-icons name='facebook' /></a>
                        <a href="mailto:ansor@info.com"><social-media-icons name='youtube' /></a>
                      </div>
                    </li>
                </ul>
            </div>
            <footer-map />
        </div>
    </div>
</template>

<script>
import SocialMediaIcons from '../../assets/Shared/SocialMediaIcons.vue'
import FooterMap from './FooterMap.vue'
export default {
  components: { SocialMediaIcons, FooterMap },
    name:'Footer'
}
</script>

<style lang="scss" scoped>
    .footer {
        background-color: #163828;
    }

    span {
        font-family: var(--montserrat);
    }

    a {
        font-family: var(--montserrat);
        line-height: 44px;
    }

    .contact-links {
        border-bottom: 1px solid #295C44;
    }

    ul {
        display: flex;
        .social-icons {
            display: flex;
            margin-top: 8px;
        }
    }

    @media screen and(max-width: 1285px) {
       
       ul {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(205px, 1fr));
        width: 600px;
       }

       h1 {
           margin-right: 42px;
       }        
    }

    @media screen and (max-width: 720px) {
        .footer {
            padding-inline: 10px;
        }

        a {
            font-size: 16px;
        }
    }

    @media screen and(max-width: 665px) {
        ul {
            width: auto;
            grid-template-columns: repeat(auto-fit, minmax(205px, 1fr));
            margin-top: 20px;
        }
        .contact-links {
            flex-direction: column;
        }
    }

    @media screen and(max-width: 467px) {
        a {
            line-height: 22px;
        }

        span {
            margin-top: 15px;
        }

        .social-icons {
            margin-top: 0 !important;
        }
    }
</style>