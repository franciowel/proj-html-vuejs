<template>
    <section>
        <div class="contain">
            <!-- text -->
            <div class="intro">
                <div class="top-title">Blog</div>
                <h2>Latest<span class="no-bold"> Post</span></h2>
                <div class="bottom-title">When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface.</div>
            </div>

            <newsCard :json="cardJson"/>

        </div>
    </section>
</template>

<script>
import latestnews from '../assets/json/latestnews.json';
import newsCard from './newsCard.vue';

export default {
    name: 'latestPost',
    components: { newsCard },
    data() {
        return {
            cardJson: latestnews,
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
@import '../assets/style/colors.scss';

section{
    background-color: $back_1;
    margin-top: 24rem;
    padding: 4.5rem 0;
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