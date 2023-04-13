<template>
<div class="pay-cards">
    <div class="container-1170">
        <div class="component-content">
            <div class="cards-container">

                <div :class="item.recomend ? 'card-recomend' : 'card-item'" v-for="item in cardList" :key="item.id">
                    <h2 class="card-title">{{ item.title }}</h2>
                    <h1 class="card-price"><span class="usd">$</span>{{ item.price }}</h1><p class="price-period">per mouth</p>
                    <ul class="card-advantages">
                        <li class="card-advantage-item" v-for="adv in item.advanteges" :key="adv">{{ adv }}</li>
                    </ul>
                    <button class="card-btn">get started</button>
                </div>

            </div>
        </div>
    </div>
</div>
</template>


<script>
export default {
    props: ['card-list'],
}
</script>


<style scoped>
.cards-container{
    justify-content: center;
    align-items: center;
    display: flex;
}
.card-advantages{
    text-align: center;
}
.card-item{
    font-family: 'Lato', sans-serif;
    border-top: 1px solid #ccd5df;
    border-bottom: 1px solid #ccd5df;
    border-radius: 5px;
    padding: 58px 35px 50px;
    background-color: #fff;
    color: #8a8a8a;
    display: flex;
    flex-direction: column;
    align-items: center;
}
.card-recomend{
    border-top: 1px solid #ccd5df;
    border-bottom: 1px solid #ccd5df;
    border-radius: 5px;
    padding: 90px 35px 80px;
    background-color: #709dca;
    color: #fff;
    display: flex;
    flex-direction: column;
    align-items: center;
    font-family: 'Lato', sans-serif;
}
.card-title{
    text-transform: uppercase;
    font-weight: 100;
    font-size: 25px;
}
.card-price{
    font-family: 'Open Sans', sans-serif;
    font-weight: 500;
    font-size: 48px;
    color: #ffbb42;
}
.price-period{
    font-weight: 100;
    text-transform: uppercase;
    font-size: 14px;
}
.card-advantages{
    margin-top: 33px;
    margin-bottom: 25px;
}
.card-advantage-item{
    padding: 15px 60px;
    text-transform: uppercase;
    border-top: 1px solid #bac0c5;
}
.card-btn{
    border-radius: 2px;
    border: 0;
    background-color: #ffbb42;
    padding: 16px 22px;
    color: #fff;
    text-transform: uppercase;
    font-size: 14px;
    cursor: pointer;
}

@media (max-width: 1200px) {
    .cards-container{
        justify-content: center;
        align-items: center;
        display: flex;
        flex-direction: column;
        gap: 50px;
    }
}
</style>