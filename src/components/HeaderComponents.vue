<template>
    <header>
        <div class="contain">
            <div class="navbar">
                <!-- logo -->
                <div class="logo">
                    <img src="../assets/img/white-logo-2.png" alt="Logo Phlox Corporate">
                </div>
                <div class="navigation flexcontain">

                    <!-- links -->
                    <div class="links">
                        <a :href="item.link" v-for="item, index in headerLinks" :key="index">{{item.text}}</a>
                    </div>

                    <!-- sign up -->
                    <div class="btn-sign">
                        <a href="#">Sign In</a>
                    </div>

                </div>
            </div>
        </div>
    </header>
</template>

<script>
export default {
    name: 'HeaderComponents',
    props: {
        headerLinks: Array,
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
@import '../assets/style/colors.scss';
header{
    height: 80px;
    background-color: $back_9;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
}
.navbar{
    height: 80px;
    display: flex;
    justify-content: space-between;
}

.logo{
    align-self: center;
}

.navigation{
    align-self: center;
}

a{
    margin: 0 14px;
    color: white;
}

.links a:first-child{
    color: $text_9;
    font-weight: 700;
}

.btn-sign{
    margin-left: 1.2rem;
}

.btn-sign a{
    background-image: linear-gradient(-90deg, #527CEB, #03A7D3E6);
    border-radius: 25px;
    padding: 0.6rem 1.2rem;
}

</style>