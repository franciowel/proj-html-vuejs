<template>
    <div class="contain">
        <div class="sponsorflex">
            <img src="../assets/img/client-1-1.png" alt="Golden">
            <img src="../assets/img/clienty-2.png" alt="Golden">
            <img src="../assets/img/clienty-3.png" alt="Golden">
            <img src="../assets/img/clienty-4.png" alt="Golden">
            <img src="../assets/img/client-5.png" alt="Golden">
        </div>
    </div>
</template>

<script>
export default {
    name: 'SponsorComponent',
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
@import '../assets/style/colors.scss';
.sponsorflex{
    display: flex;
    justify-content: space-between;
    padding: 3.6rem 0;
    img{
        width: 120px;
        height: 100%;
    }
}

</style>