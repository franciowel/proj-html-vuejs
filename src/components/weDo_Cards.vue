<template>
    <div class="contain">
        <div class="card" v-for="item, index in json" :key="index">
            <img :src="require(`../assets/img/${item.img}`)" alt="">
            <h5>{{item.job}}</h5>
            <p>{{item.description}}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'weDoCards',
    props: {
        json: Array,
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
@import '../assets/style/colors.scss';

.contain{
    display: flex;
    justify-content: space-between;
}
.card{
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    padding: 2rem 1rem;
    img{
        padding: 2rem;
    }
    h5{
        font-size: 1.5rem;
        text-align: center;
        margin: 1.5rem 0;
    }
    p{
        text-align: center;
        padding-top: 2rem;

    }
}


</style>