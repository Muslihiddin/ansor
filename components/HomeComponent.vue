<template>
<div class="home">
        <parallax />
    <div class="content"> 
        <navbar />
        <div class="div"></div>
        <services-block />
        <about-block />
        <products-block />
        <recognized-brands />
        <portfolio-block />
        <contact-block />
        <footer-block />
        <footer-bottom />
    </div>    
</div>
</template>

<script>
import AboutBlock from './About/AboutBlock.vue'
import ContactBlock from './ContactBlock/ContactBlock.vue'
import Navbar from './Navbar/Navbar.vue'
import Parallax from './Parallax/Parallax.vue'
import ProductsBlock from './Products/ProductsBlock.vue'
import PortfolioBlock from './Portfolio/PortfolioBlock.vue'
import RecognizedBrands from './RecognizedBrands/RecognizedBrandsBlock.vue'
import ServicesBlock from './ServicesBlock/ServicesBlock.vue'
import FooterBlock from './Footer/FooterBlock.vue'

export default {
    name: 'HomeComponent',
    components: {
        Parallax,
        Navbar,
        ServicesBlock,
        AboutBlock,
        ProductsBlock,
        RecognizedBrands,
        PortfolioBlock,
        ContactBlock,
        FooterBlock
    }
}        
</script>
<style lang="scss" scoped>
    .div {
        width: 95vw;
        height: 100vh;
        z-index: -10;
        pointer-events: none;
    }
</style>