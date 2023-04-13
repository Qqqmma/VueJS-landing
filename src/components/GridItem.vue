<template>
<div class="greed-item">
    <div class="container-1170">
        <div class="container-for-grid">
            <ul class="grid-container">

                <li v-for="item in arrayItems" :key="item.id" class="grid-item">
                    <div class="item-pic">
                        <img :src="item.ico" :alt="item.id">
                    </div>

                    <div class="item-text">
                        <h2 class="item-title">{{ item.title }}</h2>
                        <p class="item-description">{{ item.desc }}</p>
                    </div>
                </li>
                            
            </ul>
        </div>
    </div>
</div>
</template>


<script>
export default {
    props: ['array-items'],
}
</script>


<style scoped>
.grid-container{
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    justify-content: center;
    gap: 80px 90px;
}
.grid-item{
    display: grid;
    grid-template-columns: 83px 430px;
}
.item-title{
    text-transform: uppercase;
    font-family: 'Lato', sans-serif;
    font-weight: 700;
    font-size: 16px;
    margin-bottom: 20px;
}
.item-description{
    font-family: 'Open Sans', sans-serif;
    font-weight: 400;
    font-size: 13px;
    color: #8d8d8d;
}

@media (max-width: 1200px) {
    .grid-container{
        grid-template-columns: repeat(1, 1fr);
        justify-content: center;
    }
    .grid-item{
        justify-content: center;
    }
}
</style>