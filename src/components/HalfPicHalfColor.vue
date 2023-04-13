<template>
<div class="half-picture-half-color">
    <div class="pic-container">
        <img class="pic-item" :src="imgSrc" alt="">
    </div>
    <div class="container-1170">
        <div class="component-content">
            <div class="component-text">
                <h2 class="component-title">{{ title }}</h2>
                <p class="component-desc">{{ description }}</p>
                <button class="component-desc-btn">{{ btnDescription }}</button>
            </div>
        </div>
    </div>
</div>
</template>


<script>
export default {
    props: ['img-src', 'title', 'description', 'btn-description'],
}
</script>


<style scoped>
.half-picture-half-color{
    background: #ffc155 url("../assets/pics/about-us-section/about-us-pic.jpg") no-repeat;
    overflow: hidden;
}
.component-content{
    display: flex;
    justify-content: end;
    align-content: center;
    font-size: 0;
}
.component-title{
    margin-top: 165px;
    margin-bottom: 30px;
    font-family: 'Open Sans', sans-serif;
    font-weight: 700;
    font-size: 28px;
    text-transform: uppercase;
    color: #fff;
}
.component-desc{
    font-family: 'Open Sans', sans-serif;
    font-size: 13px;
    color: #fff;
    line-height: 1.7;
    margin-bottom: 35px;
}
.pic-container{
    font-size: 0;
    position: absolute;
}
.pic-item{
    max-width: 100%;
}
.component-text{
    width: 50%;
    max-width: 530px;
}

.component-desc-btn{
    border: 1px solid #e7ad48;
    color: #fff;
    border-radius: 1px;
    background-color: #ffc155;
    text-transform: uppercase;
    padding: 15px 32px;
    cursor: pointer;
    margin-bottom: 175px;
}

@media (max-width: 1650px) {
    .half-picture-half-color{
        background: #ffc155;
    }
    .component-content{
        display: flex;
        justify-content: center;
        align-content: center;
        font-size: 0;
    }
}
</style>