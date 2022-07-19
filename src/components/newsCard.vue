<template>
    <div class="card-contain">

        <div class="card" :class="item.entity" v-for="item, index in json" :key="index">

            <div class="head">
                <span class="date">{{item.date}}</span>
                <h4>{{item.title}}</h4>
                <span class="big">{{item.summary}}</span>
            </div>

            <div class="button">
                <a href="#">Read More</a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'newsCard',
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
    width: 100%;
    justify-content: space-between;
}
.card{
    padding: 2.5rem 1rem;
    margin: 1rem;
}

.important{
    background-image: url(../assets/img/headway-537308-unsplash-1380x703.jpg);
    border-radius: 30px;
    background-size: cover;
    display: flex;
    align-items: flex-end;
    width: 55%;
    text-align: left;
    display: flex;
    .head{
        align-self: center;
        color: $text_1;
    }
    .date{
        font-size: 0.8rem;
    }
    h4{
        font-size: 1.4rem;
        margin: 1rem 0;
    }
}


.not-important{
    background-image: linear-gradient(175deg,#0b1852 ,#527CEB);
    border-radius: 30px;
    color: $text_1;
    width: 25%;
    h4{
        font-size: 1.4rem;
        margin: 2rem 0;
    }
}

.button{
    margin: 3rem 0;
}

.button a{
    padding: 0.8rem 1.5rem;
    background-color: white;
    border-radius: 25px;
    color: black;
}

</style>