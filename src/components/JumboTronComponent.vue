<template>
    <section>
        <div class="contain">
            <div class="flexcontain">
                <!-- info -->
                <div class="info">
                    <h2>Business Planning <span>Digital Technology</span> Mondern Solution!</h2>
                    <p>When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface.</p>

                    <!-- buttons -->
                    <div class="btn-contain">
                        <a class="try" href="#">
                            Try It Now
                        </a>

                        <a class="explore" href="#">
                            Explore More
                        </a>
                    </div>
                </div>

                <!-- img -->
                <div class="image">
                    <img class src="../assets/img/header.png" alt="">
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'JumbotronComponent',
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
@import '../assets/style/colors.scss';

section{
    background-color: $back_9;
    margin-top: 80px;
}

.info{
    width: 50%;
    align-self: center;
    color: $text_1;
    h2{
        font-size: 3.5rem;
        font-weight: 600;
        line-height: 3.7rem;
    }
    span{
        display: block;
        font-weight: 500;
    }
    p{
        font-size: 1rem;
        line-height: 2rem;
        width: 80%;
        margin-top: 2rem;
        color: $text_8;
    }
}
.btn-contain{
    margin-top: 2rem;
    a{
        margin-right: 1.2rem;
        padding: 0.8rem 1.5rem;
        border-radius: 25px;
        color: $text_1;
        transition: all 0.2s ease-in-out;
    }
    .try{
            background-image: linear-gradient(90deg, #B6246E, #F9636B);
            &:hover{
                color: rgba(255, 255, 255, 1);
                box-shadow: 0 5px 15px rgba(247, 73, 140, 0.479);
            }
        }
    .explore{
            background-image: linear-gradient(90deg, #527CEB, #03A7D3E6);
            &:hover{
                color: rgba(255, 255, 255, 1);
                box-shadow: 0 5px 15px rgba(77, 124, 226, 0.4);
            }
        }
}
.image{
    height: 100%;
    img{
        padding-top: 2.2rem;
        padding-bottom: 3rem;
    }
}
</style>