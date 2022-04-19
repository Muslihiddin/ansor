<template>
    <div class="brandsPortfolio mt-12">
        <div class="airbnb brandsCard">
            <icon name="airbnb" class="svg" />
            <p class="portfolioParagraph">We give you exact quote before startin</p>
        </div>
        <div class="hubspot brandsCard brandsCard-tall">
            <icon name="hubspot" class="svg" />
            <p class="portfolioParagraph">We give you exact quote before startin</p>
        </div>
        <div class="microsoft brandsCard">
            <icon name="microsoft" class="svg" />
            <p class="portfolioParagraph">We give you exact quote before startin</p>
        </div>
        <div class="walmart brandsCard">
            <icon name="walmart" class="svg" />
            <p class="portfolioParagraph">We give you exact quote before startin</p>
        </div>
        <div class="airbnb2 brandsCard">
            <icon name="airbnb" class="svg" />
            <p class="portfolioParagraph">We give you exact quote before startin</p>
        </div>
    </div>
</template>

<script>
import Icon from '../../assets/Shared/Icon.vue'
export default {
    name: 'PortfolioBrands',
    components: { Icon },
}
</script>

<style lang='scss'>
    .brandsPortfolio {
        display: grid;
        gap: 24px;
        grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
        grid-auto-rows: 350px;
    }

    .brandsCard {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;    
        padding: 105px 74px;
        border-radius: 16px;
        text-align: center;
    }

    .svg path {
        fill: #fff;
    }

    .portfolioParagraph {
        font-family: var(--rubik);
        font-weight: 500;
        font-size: 24px;
        line-height: 38px;
        color: #fff;
        margin-top: 17px;
    }

    .airbnb {
        background-color: #F7575C;
    }

    .hubspot {
        background-color: #EE721C;
    }

    .microsoft {
        background-color: #00A3EE;
    }

    .walmart {
        background: #F7AE2E;
    }

    .airbnb2 {
        background: #3DB079;
    }

    @media screen and(min-width: 768px) {
        .brandsCard-tall {
            grid-row: span 2 / auto;
        }
    }
</style>