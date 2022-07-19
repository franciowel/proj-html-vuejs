<template>
    <section>
        <div class="contain">
            <!-- text -->
            <div class="intro">
                <div class="top-title">Testimonials</div>
                <h2>What<span class="no-bold">People Say</span></h2>
                <div class="bottom-title">When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface.</div>
            </div>

            <testimonialsCard :json="cardJson"/>

        </div>
    </section>
</template>

<script>
import testimonials from '../assets/json/testimonials.json';
import testimonialsCard from './TestimonialsCards.vue';

export default {
    name: 'peopleSay',
    components: { testimonialsCard },
    data() {
        return {
            cardJson: testimonials,
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