<template>
<div class="mobileNavbar">
    <navbar-burger @click="toggle" class="burger" :menuOpened="menuOpened" @toggle='toggle' />
    <div class="responsiveNavbar" :class="{menuOpened: menuOpened}">
        <div class="links">
            <ul>
                <li><a href="#about" @click="toggle">About</a></li>
                <li><a href="#services" @click="toggle">Our services</a></li>
                <li><a href="#portfolio" @click="toggle">Portfolio</a></li>
                <li><a href="#contact" @click="toggle">Contact</a></li>
            </ul>
        </div>
    </div>
</div>    
</template>

<script>
import NavbarBurger from './NavbarBurger.vue'
export default {
    components: { NavbarBurger },
    data() {
        return {
            menuOpened: false
        }
    },
    methods: {
        toggle() {
            this.menuOpened = !this.menuOpened
        }
    }
}
</script>

<style lang="scss" scoped>
$cubic: cubic-bezier(0.4, 0.01, 0.165, 0.99);
$menuItems: 4;

.burger {
    position: relative;
    z-index: 999;
}
.responsiveNavbar {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 0;
    padding-inline: 25px;

    display: flex;
    align-items: center;

    font-family: var(--poppins);
    font-size: 3rem;
    color: var(--Black_01);
    ul {
        position: relative;
        display: block;
        li {
            border-bottom: 1px solid #333;
            margin-top: 15px;
            transform: scale(1.15) translateY(-30px);
            opacity: 0;
            transition: transform 0.5s $cubic, opacity 0.6s $cubic;
            @for $i from 1 through $menuItems {
                &:nth-child(#{$i}) {
                    transition-delay: #{0.56 - ($i * 0.07)};
                }
            }
            a{
                display: block;
                color: transparent;
                pointer-events: none;
            }
        }
    }
}
.responsiveNavbar.menuOpened {
    height: 100%;
    transition: all 0.3s ease-in, background 0.5s ease-in;
    display: flex;

    background: rgba(0, 0, 0, 0.86);
    box-shadow: 0 4px 30px rgba(255, 255, 255, 0.1);
    backdrop-filter: blur(7.9px);
    -webkit-backdrop-filter: blur(7.9px);
    li {
        transform: scale(1) translateY(0px);
        opacity: 1;
        a {
            color: #fff;
            opacity: .9;
            pointer-events: auto;
        }
        @for $i from 1 through $menuItems {
            &:nth-child(#{$i}) {
                transition-delay: #{0.07 * $i+0.4}s;
            }
        }
    }
}

</style>