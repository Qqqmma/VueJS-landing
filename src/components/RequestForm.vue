<template>
<div class="request-form">
    <div class="container-1170">
        <form action="" class="request-form-container">
            <div class="input-container">
                <img src="../assets/pics/icons/fool-name-ico.png" alt="" class="input-icon">
                <input class="input-item name" type="text" name="name" placeholder="Fool Name">
            </div>

            <div class="input-container">
                <img src="../assets/pics/icons/email-ico.png" alt="" class="input-icon">
                <input class="input-item" type="text" name="email" placeholder="Email Adress">
            </div>

            <div class="input-container">
                <img src="../assets/pics/icons/phone-ico.png" alt="" class="input-icon">
                <input class="input-item" type="text" name="phone" placeholder="Phone Number">
            </div>
            
            <input class="submit-item" type="submit" @click.prevent :value="btnDesc.toUpperCase()">
        </form>
    </div>
</div>
</template>


<script>
export default {
    props: ['btn-desc'],
}
</script>


<style scoped>
.request-form-container{
    display: flex;
    justify-content: space-around;
}
.input-item{
    font-family: 'Open Sans', sans-serif;
    color: #b4b4b4;
    font-size: 13px;

    padding-left: 41px;
    width: 241px;
    height: 45px;
    border: 0;
    border-radius: 2px;
    background-color: #fff;
}
.input-container{
    position: relative;
}
.input-icon{
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    left: 15px;
}
.submit-item{
    font-family: 'Open Sans', sans-serif;
    font-size: 14px;
    color: #fff;

    height: 45px;
    max-width: 282px;
    cursor: pointer;
    background-color: #ffbb42;
    border: 0;
    border-radius: 2px;
    padding: 0 44px;
}

@media (max-width: 1200px) {
    .request-form-container{
        flex-direction: column;
        align-items: center;
        height: 250px;
    }
}
</style>