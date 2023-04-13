<template>
<div class="how-it-work-component">
<div class="container-1170">
    <div class="steps-container">

        <div class="step">
            <div class="step-pic">
                <img src="../assets/pics/how-it-work-ico/lock.png" alt="" class="step-ico">
            </div>
            <h2 class="step-title">step 1</h2>
            <p class="step-desc">Lorem ipsum dolor sit amet consectetur adipisicing elit. Deleniti, sed nihil eos maiores ullam eum magni facere velit qui explicabo deserunt pariatur</p>
        </div>

        <div class="step-arrow-container-top">
            <img src="../assets/pics/how-it-work-ico/btn-arrow.png" alt="" class="step-arrow-top">
        </div>

        <div class="step">
            <div class="step-pic">
                <img src="../assets/pics/how-it-work-ico/lock.png" alt="" class="step-ico">
            </div>
            <h2 class="step-title">step 2</h2>
            <p class="step-desc">Lorem ipsum dolor sit amet consectetur adipisicing elit. Deleniti, sed nihil eos maiores ullam eum magni facere velit qui explicabo deserunt pariatur</p>
        </div>

        <div class="step-arrow-container-down">
            <img src="../assets/pics/how-it-work-ico/btn-arrow.png" alt="" class="step-arrow-down">
        </div>

        <div class="step">
            <div class="step-pic">
                <img src="../assets/pics/how-it-work-ico/lock.png" alt="" class="step-ico">
            </div>
            <h2 class="step-title">step 3</h2>
            <p class="step-desc">Lorem ipsum dolor sit amet consectetur adipisicing elit. Deleniti, sed nihil eos maiores ullam eum magni facere velit qui explicabo deserunt pariatur</p>
        </div>
        
        <div class="step-arrow-container-top">
            <img src="../assets/pics/how-it-work-ico/btn-arrow.png" alt="" class="step-arrow-top">
        </div>

        <div class="step">
            <div class="step-pic">
                <img src="../assets/pics/how-it-work-ico/lock.png" alt="" class="step-ico">
            </div>
            <h2 class="step-title">step 4</h2>
            <p class="step-desc">Lorem ipsum dolor sit amet consectetur adipisicing elit. Deleniti, sed nihil eos maiores ullam eum magni facere velit qui explicabo deserunt pariatur</p>
        </div>

    </div>

    <button class="how-it-work-btn">get start now</button>
</div>
</div>
</template>


<script>

</script>


<style scoped>
.steps-container{
    display: flex;
    justify-content: center;
}
.step{
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 215px;
    text-align: center;
}
.step-pic{
    margin-bottom: 100px;
}
.step-title{
    font-family: 'Lato', sans-serif;
    text-transform: uppercase;
    font-weight: 700;
    font-size: 20px;
    margin-bottom: 30px;
}
.step-desc{
    font-family: 'Open Sans', sans-serif;
    font-size: 13px;
}
.step-arrow-container-down{
    margin: 95px -30px;
    transform: rotate(0deg);
    height: 33px;
    width: 129px;
}
.step-arrow-container-top{
    margin: -35px -30px;
    transform: rotate(180deg);
    height: 33px;
    width: 129px;
}
.how-it-work-btn{
    font-family: 'Lato', sans-serif;
    color: #fff;
    border: 0;
    border-radius: 2px;
    margin: 95px 0 150px;
    padding: 15px 30px;
    font-size: 14px;
    text-transform: uppercase;
    background-color: #ffbb42;
    cursor: pointer;
}
.container-1170{
    display: flex;
    flex-direction: column;
    align-items: center;
}

@media (max-width: 1200px) {
    .steps-container{
        display: flex;
        justify-content: center;
        flex-direction: column;
        gap: 30px;
    }
    .step-pic{
        margin-bottom: 30px;
    }
    .step-arrow-container-down{
        display: none;
    }
    .step-arrow-container-top{
        display: none;
    }
}
</style>