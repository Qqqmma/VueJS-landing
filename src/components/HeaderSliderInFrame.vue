<template>
<div class="header-slider">
    <div class="container-1170">
        <div class="header-slider-frame">
            <div class="header-slider-content">
                <div class="header-slider-container">
                    <img src="../assets/pics/notebook-frame.png" alt="" class="header-frame-pic">
                    <div class="slider-container">
                        <ul :style="sliderLineStyle" id="slider-line">
                            <li v-for="item in sliderItems" :key="item" class="slider-item">
                                <img :src="item.src" :alt="item.id" class="slider-img">
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="slider-btns">
                    <button 
                    v-for="i in sliderLength" :key="i"
                    @click="sliderPosition = i - 1"
                    :class="{'active-btn': sliderPosition == i - 1,}"
                    class="slider-btn-item">{{   }}</button>
                </div>
            </div>

        </div>
    </div>
</div>
</template>


<script>
export default {
    data() {
        return {
            sliderPosition: 0,
        }
    },
    props: ['slider-items'],
    methods: {
        next() {
            this.sliderPosition++;
            if (this.sliderPosition >= this.sliderLength) {
                this.sliderPosition = 0;
            }
        },
        previous() {
            this.sliderPosition--;
            if (this.sliderPosition < 0) {
                this.sliderPosition = this.sliderLength - 1;
            }
        },
        changeBtnBorder() {
            
        },
    },
    computed: {
        sliderLength() {
            return this.sliderItems.length;
        },
        sliderLineStyle() {
            return {
                width: this.sliderLength * 100 + "%",
                left: "-" + (this.sliderPosition * 100 + "%"),
            };
        },
    }
}
</script>


<style scoped>
.header-slider-content{
    display: flex;
    align-items: center;
    flex-direction: column;
}
.header-slider-container{
    position: relative;
    height: 344px;
    width: 648px;
}
.header-frame-pic{
    position: absolute;
}
.slider-container{
    position: absolute;
    overflow: hidden;   

    background-color: #ffb6b6;
    height: 250px;
    width: 450px;
    top: 20px;
    left: 100px;
}



#slider-line{
    position: absolute;
    left: 0%;
    display: flex;
    transition: .2s;
}
.slider-item{
    width: 100%;
}
.slider-img{
    width: 100%;
}
.slider-btn-item{
    border: 0;
    height: 16px;
    width: 16px;
    padding: 0;
    border-radius: 20px;
    background-color: #fff;
    margin: 23px 3px 0;
    transition: .2s;
    border: 2px solid #e1e2e3;

    cursor: pointer;
}
.active-btn{
    border: 2px solid #1ca8dd;
}

@media (max-width: 690px) {
    .header-frame-pic{
        display: none;
    }
    .header-slider-container{
        position: relative;
        height: 344px;
        width: 600px;
    }
}
</style>