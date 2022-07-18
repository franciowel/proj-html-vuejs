<template>
    <section>
        <div class="contain">
            <div class="flexcontain">
                <!-- info -->
                <div class="info">
                    <h2>Business Planning <span>Digital Technology</span> Mondern Solution!</h2>
                    <p>When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface.</p>
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
.image{
    height: 100%;
    img{
        padding: 2rem 0;
    }
}
</style>