<template>
    <section>
        <div class="contain">
            <!-- text -->
            <div class="intro">
                <div class="top-title">Our Services</div>
                <h2>What<span class="no-bold">We Do</span></h2>
                <div class="bottom-title">When, while the lovely valley teems with vapour around meand the</div>
            </div>

            <weDoCards :json="cardJson"/>

            <!-- buttons -->
            <div class="btn-contain">
                <a class="view" href="#">
                    View All Services
                </a>
            </div>
        </div>
    </section>
</template>

<script>
import whatweDo from '../assets/json/whatweDo.json';
import weDoCards from './weDo_Cards.vue';

export default {
    name: 'whatWeDo',
    components: { weDoCards },
    data() {
        return {
            cardJson: whatweDo,
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
@import '../assets/style/colors.scss';

section{
    background-color: $back_1;
    padding: 3rem 0;
}

.btn-contain{
    margin: 3.2rem 0;
    text-align: center;
    a{
        margin-right: 1.2rem;
        padding: 0.8rem 1.7rem;
        border-radius: 25px;
        color: $text_1;
    }
    .view{
            background-image: linear-gradient(90deg, #B6246E, #F9636B);
        }
}

</style>