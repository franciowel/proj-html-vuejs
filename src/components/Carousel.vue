<template>
    <section>
        <div class="contain">
            <!-- text -->
            <div class="intro">
                <div class="top-title">Portfolio</div>
                <h2>latest<span class="no-bold">work</span></h2>
                <!-- <div class="bottom-title"></div> -->
            </div>

            <!-- slider -->

        </div>
    </section>
</template>

<script>

export default {
    name: 'sliderCarousel',
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
@import '../assets/style/colors.scss';

section{
    background-color: $back_1;
    padding: 3rem 0;
}
.intro{
    text-align: left;
}

</style>