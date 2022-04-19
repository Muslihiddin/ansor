<template>
    <nav :class="{change_color: scrollPosition > 50}">
        <div class="container xl:max-w-7xl mx-auto px-2.5 sm:px-0">
            <div class="logo">
                <a href="#home"><icon name='logo' /></a>
            </div>
            <div class="links">
                <ul>
                    <li><a href="#about">About</a></li>
                    <li><a href="#services">Our services</a></li>
                    <li><a href="#portfolio">Portfolio</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
                <navbar-button />
            </div>
            <navbar-responsive class="burgerMenu" />
        </div>
    </nav>
</template>

<script>
import Icon from '../../assets/Shared/Icon.vue'
import NavbarButton from './NavbarButton.vue'
import NavbarResponsive from './NavbarResponsive.vue'
export default {
    name: 'Navbar',
    components: { 
        Icon,
        NavbarButton,
        NavbarResponsive
    },
    data() {
        return {
            scrollPosition: null,
        }
    },
    methods: {
        updateScroll() {
            this.scrollPosition = window.scrollY
        }
    },
    mounted() {
        window.addEventListener('scroll', this.updateScroll)
    }
}
</script>

<style lang="scss" scoped>
nav {
    position: fixed;
    z-index: 10;
    width: 100%;
    max-height: 80px;
    padding: 16px 10px;
    margin-inline: auto;
    background-color: transparent;
    transition: all 0.4s ease-in-out;
}

.change_color {
    background-color: rgba(0,0,0,.861);;
}

.container {
    display: flex;
    align-items: center;
    justify-content: space-between;

    max-width: 1280px;
    margin-inline: auto;
}

.links {
    display: flex;
    align-items: center;

    ul {
        display: flex;
        align-items: center;
        column-gap: 40px;

        a{
            font-family: var(--poppins);
            font-weight: 500;
            font-size: 16px;
            line-height: 24px;
            color: #fff;
            transition: 0.1s ease;

            &:hover {
                color: var(--Green_01);
            }
        }
    }
}

.burgerMenu {
    display: none;
}

@media screen and(max-width: 980px) {
    .links {
        display: none;
    }
    .burgerMenu {
        display: block;
    }
}
</style>