<template>
    <div class="foot">

        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.1.1/css/all.min.css" integrity="sha512-KfkfwYDsLkIlwQp6LFnl8zNdLGxu9YAA1QvwINks4PhcElQSvqcyVLLD9aMhXd13uQjoXtEKNosOWaZqXgel0g==" crossorigin="anonymous" referrerpolicy="no-referrer" />

        <div class="contain services">
            <div class="mail-list">
                <div class="text-intro">
                    <h2>We Offer Awesome Services</h2>
                    <p>When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface.</p>
                </div>

                <div class="input">
                    <input type="text" placeholder="Enter Your Email Address">
                    <a href="#">Subscribe</a>
                </div>
            </div>
        </div>

        <footer>
            <div class="foot-links">
                <div class="contain foot-content">

                    <div class="info">
                        <img src="../assets/img/white-logo-2.png" alt="Logo Phlox Corporate">
                        <p>
                            When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface.
                        </p>
                    </div>

                    <div class="columns">
                        
                        <div class="links">
                            <h5>
                                Quick Links
                            </h5>
                            <a :href="item.link" v-for="item, index in quickLinks" :key="index">{{item.text}}</a>
                        </div>

                        <div class="links">
                            <h5 class="second-title">
                                Resources
                            </h5>
                            <a :href="item.link" v-for="item, index in resourcesLinks" :key="index">{{item.text}}</a>
                        </div>

                    </div>

                    <div class="contact">

                        <h5>
                            Contact Us
                        </h5>

                        <div class="address">
                            <h6>
                                Address:
                                <span>
                                    Patricia C. Amedee 4401 Waldeck Street Grapevine Nashville, Tx 76051
                                </span>
                            </h6>
                        </div>

                        <h6>
                            Phone:
                            <span>
                                Patricia C. Amedee 4401 Waldeck Street Grapevine Nashville, Tx 76051
                            </span>
                        </h6>

                        <h6>
                            Email:
                            <span>
                                Patricia C. Amedee 4401 Waldeck Street Grapevine Nashville, Tx 76051
                            </span>
                        </h6>


                    </div>
                </div>
            </div>

            <div class="credits">
                <div class="contain">

                    <div class="utilities">

                        <div class="copy">
                            &copy; Francesco Spina, 2022.
                        </div>

                        <div class="socials">
                            <ul class="flexcontain">
                                <li>
                                    <a href="#">
                                        <i class="fa-brands fa-instagram"></i>
                                    </a>
                                </li>

                                <li>
                                    <a href="#">
                                        <i class="fa-brands fa-linkedin-in"></i>
                                    </a>
                                </li>

                                <li>
                                    <a href="#">
                                        <i class="fa-brands fa-facebook-f"></i>
                                    </a>
                                </li>

                                <li>
                                    <a href="#">
                                        <i class="fa-brands fa-twitter"></i>
                                    </a>
                                </li>
                            </ul>

                            <div class="buttons">

                                <a class="arrow-home" href="#">
                                    <i class="fa-solid fa-arrow-up"></i>
                                </a>

                                <a class="support" href="#">
                                    <i class="fa-solid fa-comment"></i>
                                </a>

                            </div>

                        </div>

                    </div>

                </div>
            </div>
        </footer>
    </div>
</template>

<script>
export default {
    name: 'FooterComponent',
    props: {
        quickLinks: Array,
        resourcesLinks: Array,
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
@import '../assets/style/colors.scss';

.services{
    background-image: linear-gradient(90deg, #B6246E, #F9636B);
    height: 120px;
    border-radius: 35px;
    top: 100px;
    position: relative;
    padding: 8rem 0;
}

footer{
    padding-top: 10rem;
    background-color: $back_9;
    width: 100%;
    .foot-links{
        border-bottom: 1px solid $text_10;
        padding-bottom: 3rem;
    }
}

.mail-list{
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 2.8rem;
    height: 100%;
}

.foot-content{
    display: flex;
    justify-content: space-between;
}

.text-intro{
    display: flex;
    flex-direction: column;
    color: $text_1;
    h2{
        font-size: 2.8rem;
    }
    p{
        font-size: 1.1rem;
        margin-top: 1.2rem;
    }
}

.input{
    display: flex;
    justify-content: space-between;
    background-color: white;
    border-radius: 25px;
    padding-left: 2rem;
    input{
        border: none;
        margin-right: 2rem;
        width: 200px;
        & :focus-visible{
            border: 0;
        }
    }
    a{
        margin: 3px 5px;
        padding: 0.8rem 1.5rem;
        border-radius: 25px;
        color: $text_1;
        background-image: linear-gradient(90deg, #527CEB, #03A7D3E6);
    }
}

.info{
    width: 20%;
    padding: 2rem 0;
    img{
        margin-bottom: 2rem;
    }
    p{
        color: $text_10;
        width: 80%;
    }
}

.columns{
    display: flex;
    justify-content: space-between;
    width: 50%;
    padding: 0 2rem;
    .links{
        display: flex;
        flex-direction: column;
    }
    .links a{
        color: $text_10;
        font-size: 1.1rem;
        margin-bottom: 0.3rem;
    }
    h5{
        font-size: 1.2rem;
        color: $text_1;
        margin-bottom: 1.2rem;
    }
    .second-title{
        margin-right: 2rem;
    }
}

.contact{
    width: 25%;
    color: $text_1;
    h5{
        font-size: 1.2rem;
    }
    .address{
        margin: 2rem 0;
    }
    h6{
        font-size: 1.1rem;
        font-weight: 400;
    }
    span{
        color: $text_10;
    }
}

.utilities{
    display: flex;
    justify-content: space-between;
    padding: 1rem 0;
    .copy{
        color: $text_10;
    }
    ul{
        list-style: none;
        li{
            margin-right: 15px;
        }
        a{
            color: $text_1;
        }
    }
    .socials{
        display: flex;
    }
    .buttons{
        margin-left: 2rem;
        width: 100%;
        height: 100%;
        position: relative;
    }
    .arrow-home{
        color: $text_10;
        background-color: $text_1;
        border: 1px solid $text_1;
        height: 35px;
        width: 35px;
        display: inline-block;
        text-align: center;
        line-height: 30px;
        border-radius: 50%;
        position: absolute;
        top: -18px;
        left: -15px;
    }
    .support{
        color: $text_1;
        font-size: 1.2rem;
        background-color: $back_3;
        border: 1px solid $back_3;
        height: 45px;
        width: 45px;
        display: inline-block;
        text-align: center;
        line-height: 45px;
        border-radius: 50%;
        margin-left: 3rem;
    }
}
</style>