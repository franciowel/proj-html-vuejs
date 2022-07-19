<template>
    <section>
        <div class="contain">
            <!-- text -->
            <div class="intro-alt">
                <div class="top-title">Price List</div>
                <h2>Our<span class="no-bold">Pricing</span></h2>
                <div class="bottom-title">When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface.</div>
            </div>

            <div class="cards">
                <priceCards :json="cardJson"/>
            </div>

        </div>
    </section>
</template>

<script>
import pricing from '../assets/json/pricing.json';
import priceCards from './PriceCards.vue';

export default {
    name: 'priceList',
    components: { priceCards },
    data() {
        return {
            cardJson: pricing,
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
@import '../assets/style/colors.scss';

section{
    background-color: $back_9;
    padding-top: 3rem;
    padding-bottom: 14rem;
    margin-bottom: 10rem;
}

.contain{
    position: relative;
}

.intro-alt{
    text-align: center;
    margin-bottom: 6rem;
    h2{
        font-size: 2.5rem;
        color: $text_1;
    }
    .no-bold{
        font-weight: 400;
        margin-left: 10px;
    }
    .top-title{
        color: $text_9;
        margin: 1.5rem 0;
    }
    .bottom-title{
        color: $text_18;
        margin: 1.5rem 0;
        font-size: 1.1rem;
        color: $text_1;
    }
}

.cards{
    position: absolute;
    top: 180px;
    width: 100%;
}

</style>