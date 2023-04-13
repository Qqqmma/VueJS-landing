<template>
    <div class="header-component">
        <header class="header">
            <div class="container-1170">
                <nav class="header-nav-container">
                    <div class="header-logo">
                        <img src="../assets/pics/logo.png" alt="logo">
                    </div>
                    <ul class="header-list">
                        <li class="header-list-item"><a href="#home" class="header-list-item-link active">home</a></li>
                        <li class="header-list-item"><a href="#service" class="header-list-item-link">service</a></li>
                        <li class="header-list-item"><a href="#about-us" class="header-list-item-link">about us</a></li>
                        <li class="header-list-item"><a href="#pricing-table" class="header-list-item-link">pricing table</a></li>
                        <li class="header-list-item"><a href="#how-it-work" class="header-list-item-link">how it work</a></li>
                        <li class="header-list-item"><a href="#happy-clients" class="header-list-item-link">happy client</a></li>
                        <li class="header-list-item"><a href="#contact-us" class="header-list-item-link">contact us</a></li>
                    </ul>

                    <div class="humburger">
                        <img src="../assets/pics/header-btns/burger-btn.png" alt="" class="humburger-item">
                    </div>
                </nav>
            </div>
        </header>
    </div>
</template>

<script>
export default {
    data() {
        return {
            showStatus: false,
        }
    },
    methods: {
        showList() {
            this.showStatus = !this.showStatus;
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
a{
    text-decoration: none;
    color: #000;
}
li{
    font-family: 'Lato', sans-serif;
    font-weight: 400;
    font-size: 14px;
    list-style-type: none;
}
ul{
    margin-left: 0;
    padding-left: 0;
}
.header-component{
    background-color: #fff;
    z-index: 1000;
    position: fixed;
    width: 100%;
    border-bottom: 1px solid #b4b4b4;
}
.header{
    padding: 20px 0;
}
.header-nav-container{
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.header-list{
    display: flex;
    text-transform: uppercase;
}
.container-1170{
    margin: 0 auto;
    max-width: 1200px;
    padding: 0 15px;
}
.header-list-item{
    margin-left: 45px;
}
.active{
    font-family: 'Lato', sans-serif;
    font-weight: 400;
    font-size: 14px;
    margin-right: -25px;
    margin-top: -50%;
    border: 0;
    background-color: #ffbb42;
    border-radius: 3px;
    color: #fff;
    padding: 5px 20px;
    cursor: pointer;
}
.humburger-item{
    height: 30px;
    display: none;
}
.humburger{
    position: absolute;
}
@media (max-width: 1200px) {
    .header-list-item{
        display: none;
    }
    .humburger-item{
        height: 30px;
        display: block;
    }
    .humburger{
        position: relative;
    }
}
</style>