<template>
    <div class="card-contain">
        <div class="card" :class="item.identity" v-for="item, index in json" :key="index">
            <div class="head">
                <h3>{{item.title}}</h3>
                <span>{{item.type}}</span>
                <div class="upper-lateral">
                    &dollar;
                </div>
                <div class="price">
                    <span class="big">{{item.price}}</span>
                    <span>Per Month</span>
                </div>
            </div>

            <div class="marked">
                Creative
                <span class="not-marked">
                    {{item.creative}}
                </span>
            </div>

            <div class="marked">
                Vibrant
                <span class="not-marked">
                    {{item.vibrant}}
                </span>
            </div>

            <div class="marked">
                Eye
                <span class="not-marked">
                    {{item.eye}}
                </span>
            </div>

            <div class="marked">
                Extreme
                <span class="not-marked">
                    {{item.extreme}}
                </span>
            </div>

            <div class="marked">
                Exeptional
                <span class="not-marked">
                    {{item.exceptional}}
                </span>
            </div>

            <div class="button">
                <a href="#">Order Now
                    <span>
                        <i class="fa-solid fa-arrow-right-long"></i>
                    </span>
                </a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'priceCards',
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
    display: flex;
    flex-wrap: wrap;
    flex-direction: column;
    text-align: center;
    padding: 5rem 9.5rem;
    h3{
        font-size: 2.1rem;
        text-align: center;
        margin-bottom: 1rem;
    }
    .big{
        display: block;
        font-size: 4.5rem;
        font-weight: 600;
        margin-bottom: 0.5rem;
    }
    .price{
        margin-top: 0.2rem;
        margin-bottom: 1.8rem;
    }
    .upper-lateral{
        text-align: left;
        margin-top: 1.4rem;
    }
    .marked{
        margin-bottom: 1.2rem;
        font-weight: 600;
        .not-marked{
            font-weight: 400;
        }
    }
}

.button{
    margin-top: 3rem;
}

.even{
    background-color: $text_1;
    border-radius: 30px;
    box-shadow: 8px 10px 180px #4e4e4e;
    .button a{
        margin-right: 1.2rem;
        padding: 0.8rem 1.5rem;
        font-weight: 600;
        border-radius: 25px;
        color: $text_1;
        transition: all 0.2s ease-in-out;
        &:hover{
                color: rgba(255, 255, 255, 1);
                box-shadow: 0 5px 15px rgba(247, 73, 140, 0.479);
            }
        background-image: linear-gradient(180deg, #B6246E, #F9636B);
         span{
            margin-left: 1rem;
        }
    }
}

.odd{
    color: $text_1;
    background-image: linear-gradient(90deg, #B6246E, #F9636B);
    border-radius: 30px;
    .button a{
        margin-right: 1.2rem;
        font-weight: 600;
        padding: 0.8rem 1.5rem;
        border-radius: 25px;
        color: #B6246E;
        background-color: white;
        span{
            margin-left: 1rem;
        }
    }
}
</style>