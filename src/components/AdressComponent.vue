<template>
<div class="adress-component">
    <div class="dot-map-container">
        <div class="container">

            <div class="circle-container">
                <div class="adress-container">
                    <div class="title">address</div>
                    <address class="address">
                        Business street <br>
                        Second north section <br>
                        Bavani nagar. 88769 <br>
                        Call: +987-9999-111
                    </address>
                    <p class="email">info@businessfase.com</p>
                </div>
            </div>

            <div class="map-pic-container">
                <img src="../assets/pics/dotted-map.png" alt="" class="dot-map-img">
            </div>
            
            <img src="../assets/pics/logo.png" alt="" class="map-logo">
        </div>
    </div>
</div>
</template>


<script>

</script>


<style scoped>
.title{
    text-transform: uppercase;
    font-weight: 700;
    color: #fff;
    margin-bottom: 20px;
    font-size: 20px;
    font-family: 'Lato', sans-serif;
}
.address{
    font-family: 'Lato', sans-serif;
    color: #fff;
    font-weight: 100;
    font-size: 14px;
    line-height: 1.5;
    margin-bottom: 10px;
}
.email{
    font-family: 'Lato', sans-serif;
    color: #ffbb42;
}
.adress-container{
    position: absolute;
    background-color: #394b50;
    height: 163px;
    width: 163px;
    text-align: center;
    padding: 70px 70px 70px 70px;
    border-radius: 2000px;
    top: 20px;
    left: 400px;
}
.adress-container::after{
    content: ''; 
    position: absolute;
    right: 135px; top: 305px;
    transform: rotate(90deg);
    border: 10px solid transparent;
    border-left: 20px solid #394b50;
}

.dot-map-container{
    display: flex;
    justify-content: center;
    margin-top: 50px;
}
.container{
    position: relative;
}
.dot-map-img{
    padding-bottom: 55px;
    width: 100%;
    border-bottom: 1px solid #e3e7ec;
}
.map-logo{
    position: absolute;
    bottom: 215px;
    right: 525px;
}
.map-pic-container{
    overflow: hidden;
}

@media (max-width: 1200px) {
    .dot-map-img{display: none;}
    .adress-container{
        position: relative;
        height: 163px;
        width: 163px;
        text-align: center;
        padding: 70px 70px 70px 70px;
        border-radius: 2000px;
        top: 0px;
        left: 0px;
    }
    .adress-container::after{
        content: ''; 
        position: relative;
        right: 0; top: 0;
        transform: rotate(90deg);
        border: 0 solid transparent;
        border-left: 20px solid #394b50;
    }
    .map-logo{
        display: none;
    }
}
</style>