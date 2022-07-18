<template>
    <header>
        <div class="contain">
            <div class="navbar">
                <!-- logo -->
                <div class="logo">
                    <img src="../assets/img/white-logo-2.png" alt="Logo Phlox Corporate">
                </div>
                <!-- links -->
                <div>
                    <a :href="item.link" v-for="item, index in headerLinks" :key="index">{{item.text}}</a>
                </div>
                <!-- sign up -->
                <div>
                    <a href="#">Sign Up</a>
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