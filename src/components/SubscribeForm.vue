<template>
<div class="contact-us">
    <div class="container-1170">
        <div class="contact-container">
            <form class="contact-us-form">
                <div class="input-container">
                    <img src="../assets/pics/icons/fool-name-ico.png" alt="" class="input-icon">
                    <input class="input-item name" type="text" name="name" placeholder="Name">
                </div>

                <div class="input-container">
                    <img src="../assets/pics/icons/email-ico.png" alt="" class="input-icon">
                    <input class="input-item input-mail" type="text" name="email" placeholder="Email">
                </div>
                <input class="submit-item" type="submit" @click.prevent :value="btnDesc.toUpperCase()">
            </form>
        </div>
    </div>
</div>
</template>


<script>
export default {
    data() {
        return {
            column: {
                'flex-direction': 'column', 
                'align-items': 'center', 
                'height': '250px',
            },
            row: {'flex-direction': 'row'},
        }
    },
    props: ['btn-desc', 'form-direct'],
    methods: {
        formDirection(text) {
            if (text === 'row') return this.row;
            if (text === 'column') return this.column;
        }
    }
}
</script>


<style>
.contact-us-form{
    display: flex;
    justify-content: center;
    gap: 10px;
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
    padding: 0 55px;
}
.input-item{
    font-family: 'Open Sans', sans-serif;
    color: #b4b4b4;
    font-size: 13px;

    padding-left: 41px;
    width: 241px;
    height: 45px;
    border: 1px solid #cbcbcb;
    border-radius: 2px;
    background-color: #fff;
}
.input-mail{
    width: 380px;
}

@media (max-width: 1200px) {
    .contact-us-form{
        flex-direction: column;
        align-items: center;
    }
}
</style>