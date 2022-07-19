<template>
    <div class="card-contain">

        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.1.1/css/all.min.css" integrity="sha512-KfkfwYDsLkIlwQp6LFnl8zNdLGxu9YAA1QvwINks4PhcElQSvqcyVLLD9aMhXd13uQjoXtEKNosOWaZqXgel0g==" crossorigin="anonymous" referrerpolicy="no-referrer" />

        <div class="card" v-for="item, index in json" :key="index">

            <img :src="require(`../assets/img/${item.pic}`)" alt="">

            <div class="stars">
                <i v-for="n in 5" :key="n" class="fa-solid fa-star" :class="{'fill': n <= (item.rate) }"></i>
            </div>
            <p>{{item.text}}</p>
            <h5>{{item.name}}</h5>
            <p>{{item.job}}</p>
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

.card-contain{
    display: flex;
    justify-content: space-between;
    margin-top: 4rem;
}

.card{
    text-align: center;
    padding: 1rem 6rem;
}

img{
    width: 100px;
    border: 4px solid $text_12;
    border-radius: 50%;
    margin-bottom: 1rem;
}

.stars{
    margin-bottom: 1rem;
    .fill{
        color: $text_9;
    }

}

p{
    margin-bottom: 1rem;
    font-size: 1rem;
}

h5{
    margin-bottom: 1rem;
    font-size: 0.8rem;
}



</style>