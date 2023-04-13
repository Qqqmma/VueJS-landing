<template>
<footer class="footer">
    <div class="container-1170">

        <ul class="footer-list">
            <li class="footer-content-item"><a href="#home">home</a></li>
            <li class="footer-content-item"><a href="#service">service</a></li>
            <li class="footer-content-item"><a href="#about-us">about us</a></li>
            <li class="footer-content-item"><a href="#pricing-table">pricing table</a></li>
            <li class="footer-content-item"><a href="#how-it-work">how it work</a></li>
            <li class="footer-content-item"><a href="#happy-clients">happy clients</a></li>
            <li class="footer-content-item"><a href="#contact-us">Contact us</a></li>
        </ul>

        <div class="footer-number">
            <img src="../assets/pics/footer-icons/phone.png" alt=""> <span class="number">+987 9976 999</span>
        </div>

        <div class="social-media">
            <a href="#!" class="social-media-link">
                <img src="../assets/pics/footer-icons/twiter.png" alt="twiter" class="social-ico">
            </a>
            <a href="#!" class="social-media-link">
                <img src="../assets/pics/footer-icons/facebook.png" alt="twiter" class="social-ico">
            </a>
            <a href="#!" class="social-media-link">
                <img src="../assets/pics/footer-icons/google.png" alt="twiter" class="social-ico">
            </a>
            <a href="#!" class="social-media-link">
                <img src="../assets/pics/footer-icons/linkedin.png" alt="twiter" class="social-ico">
            </a>
        </div>

    </div>
</footer>
</template>


<script>

</script>


<style scoped>
a{
    text-decoration: none;
    color: #000;
}

.footer-list{
    text-transform: uppercase;
    font-family: 'Lato', sans-serif;
    font-size: 13px;
    display: flex;
    gap: 35px;
    justify-content: center;
    margin-bottom: 30px;
}
.footer-number{
    text-align: center;
}
.number{
    font-family: 'Lato', sans-serif;
    font-size: 22px;
}
.social-media{
    margin-top: 20px;
    margin-bottom: 55px;
    display: flex;
    justify-content: center;
    gap: 20px;
}

@media (max-width: 1200px) {
    .footer-list{
        flex-direction: column;
        align-items: center;
    }
}
</style>