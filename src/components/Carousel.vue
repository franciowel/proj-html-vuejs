<template>
    <section>
        <div class="contain">
            <!-- text -->
            <div class="intro">
                <div class="top-title">Portfolio</div>
                <h2>latest<span class="no-bold">work</span></h2>
                <!-- <div class="bottom-title"></div> -->
            </div>

            <!-- slider -->

                <div class="flexslider card">
                    <div v-for="item, index in slidesArray" :key="index" :class="currentActive === index ? '' : 'hidden'">
                        <img :src="require(`../assets/img/${item.img}`)" alt="testimonials">
                        <div class="text" :class="currentActive === index ? 'active': '' " >
                            <h4>{{item.title}}</h4>
                            <p class="category">{{item.category}}</p>
                        </div>
                    </div>
                </div>

            <div class="flex-circles">
                <div v-for="items, index in slidesArray" :key="index" class="circle color" :class="currentActive === index ? 'active': '' " @click="selectThis(index)">
                </div>
            </div>

        </div>
    </section>
</template>

<script>
import slides from '../assets/json/slides.json'

export default {
    name: 'sliderCarousel',
    methods: {
        setCurrentActive() {
        setInterval(() => {
                
            if (this.currentActive < this.slidesArray.length - 1) {
                this.currentActive ++
            } 

            else if (this.currentActive === this.slidesArray.length - 1) {
                this.currentActive = 0
            }
            }, 6000);
        },
        
        selectThis(index) {
            this.currentActive = index
        }
    },
    data () {
        return {
            slidesArray: slides,
            currentActive: 0,
        }
    },
    created() {
        this.setCurrentActive();
    }   

}
</script>

<style lang="scss" scoped>
@import '../assets/style/common.scss';
@import '../assets/style/colors.scss';

section{
    background-color: $back_1;
    padding: 3rem 0;
    overflow-x: hidden;
}
.intro{
    text-align: left;
}

.flexslider{
    display: flex;
    padding: 2rem 0;
    img{
        width: 90%;
        border-top-left-radius: 30px;
        border-top-right-radius: 30px;
    }
    .text{
        line-height: 35px;
        width: 90%;
        height: 35px;
        &.active {
        background-color: $text_9;
        border-bottom-left-radius: 10px;
        border-bottom-right-radius: 10px;
        color: $text_1;
        }
        display: flex;
        flex-direction: row;
        h4{
            padding: 0 1rem;
        }
    }
}
.hidden{
    opacity: 50%;
}

.color{
    background-color: white;
    border: 1px solid $text_9;
    margin: 0 5px;
    &.active {
        background-color: $text_9;
    }
}
.flex-circles {
    display: flex;
    justify-content: center;
    align-items: center;
}

.circle {
    width: 15px;
    height: 15px;
    border-radius: 50%;
}
</style>