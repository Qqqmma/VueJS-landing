<template>
<div class="comments-component">
    <div class="container-1170">
        <div class="comments-container">
            <div class="comment-grid">

                <div class="comment-item" v-for="item in commentsList" :key="item.id">

                    <div class="comment-img-container">
                        <img :src="item.userPicture" alt="user img" class="comment-img">
                    </div>

                    <div class="comment-text">
                        <p class="comment-desc">
                            <img class="open-ckobka" src="../assets/pics/skobochka.png" alt="">
                            {{ item.description }}
                            <span class="ckobka-container"><img class="close-ckobka" src="../assets/pics/skobochka.png" alt=""></span>
                        </p>
                        <div class="user">
                            <h3 class="user-name">{{ item.userName }},</h3> <h3 class="user-function">{{ item.userFunction }}</h3>
                        </div>
                    </div>

                </div>

            </div>
        </div>
    </div>
</div>
</template>


<script>
export default {
    props: ['comments-list']
}
</script>


<style scoped>
.comment-grid{
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px 35px;
}
.comment-img-container{
    font-size: 0;
}
.comment-item{
    border-radius: 3px;
    padding: 45px 30px 55px;
    display: flex;
    gap: 30px;
    background-color: #fff;
}
.comment-desc{
    position: relative;
    font-family: 'Open Sans', sans-serif;
    line-height: 22px;
    color: #7b7b7b;
    font-size: 13px;
}
.open-ckobka{
    position: absolute;
    left: -15px;
}
.ckobka-container{
    position: relative;
}
.close-ckobka{
    transform: rotate(180deg);
    left: 5px;
    bottom: -5px;
    position: absolute;
}
.user{
    font-family: 'Lato', sans-serif;
    display: flex;
    text-transform: uppercase;
    margin-top: 30px;
}
.user-name{
    color: #f78948;
    padding-right: 10px;
}

@media (max-width: 1200px) {
    .comment-grid{
        grid-template-columns: repeat(1, 1fr);
    }
}
</style>