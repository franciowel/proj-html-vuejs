<template>
    <section>
        <div class="contain">
            <div class="flexcontain">
                <!-- img -->
                <div class="image">
                    <img class src="../assets/img/men-data.png" alt="">
                </div>
                
                <div class="info">
                    <span class="oculus">Start your Project</span>
                    <h2>Grow your Business <span>With our Strategy!</span></h2>
                    <p>
                        When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface.
                        When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface.
                    </p>

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

            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'SecondJumbo',
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
@import '../assets/style/colors.scss';

section{
    background-color: $back_9;
}
.flexcontain{
    justify-content: space-between;
}
.info{
    width: 50%;
    align-self: center;
    color: $text_1;
    .oculus{
        margin-bottom: 1.8rem;
        font-size: 1.2rem;
    }
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
    }
    .try{
            background-image: linear-gradient(90deg, #B6246E, #F9636B);
        }
    .explore{
            background-image: linear-gradient(90deg, #527CEB, #03A7D3E6);
        }
}
.image{
    height: 100%;
    img{
        width: 80%;
        padding: 3.2rem 0;
    }
}
</style>