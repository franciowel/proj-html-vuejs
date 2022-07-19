<template>
    <div class="card-contain">

        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.1.1/css/all.min.css" integrity="sha512-KfkfwYDsLkIlwQp6LFnl8zNdLGxu9YAA1QvwINks4PhcElQSvqcyVLLD9aMhXd13uQjoXtEKNosOWaZqXgel0g==" crossorigin="anonymous" referrerpolicy="no-referrer" />

        <div class="card" v-for="item, index in json" :key="index">
            <img :src="require(`../assets/img/${item.img}`)" alt="">

            <div class="stars">
                <i v-for="n in 5" :key="n" class="fa-regular fa-star" :class="{'gold': n <= voteCalc(item.rate) }"></i>
            </div>

            <h5>{{item.job}}</h5>
            <p>{{item.text}}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'testimonialCards',
    props: {
        json: Array,
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
@import '../assets/style/colors.scss';



</style>