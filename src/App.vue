<template>
  <header-component/>
  <div class="header-desc" id="home">
    <section-title class="header-title" color="white" title="boost up your local busines" description="Our services is the best in our contry!!!"></section-title>
    <request-form class="header-form" btn-desc="request a quate"/>
    <header-slider :slider-items="headerSliderPics"/>
  </div>

  <section class="our-services" id="service">
    <section-title class="our-services-title" color="black" title="our services" description="Lorem ipsum is symply dummy Business industry."></section-title>
    <grid-item class="our-services-items" :array-items="ourServicesList"/>
    <half-pictere-half-color id="about-us" title="about us" description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Maxime aspernatur quae ipsam aliquam, eius ipsa corporis sed rem adipisci assumenda odio sunt ex fugit perferendis ratione maiores aut laboriosam voluptatibus?" btn-description="read more"/>
  </section>

  <section class="our-price" id="pricing-table">
    <section-title class="price-title" title="choose your price" description="Lorem ipsum is symply dummy Business industry." color="black"/>
    <pay-cards :card-list="priceCards"/>
  </section>

  <section class="how-it-work" id="how-it-work">
    <section-title class="how-it-work-title" title="how it works" description="Lorem Ipsum is simply dummy Busines Industry!" color="black"/>
    <path-component/>
  </section>

  <section class="comments" id="happy-clients">
    <section-title class="comments-title" title="happy clients" description="We are explain who is using our business solutions" color="white"/>
    <comments-component :comments-list="commentsList"/>
  </section>

  <section class="contacts" id="contact-us">
    <section-title class="contact-title" color="black" title="newsletter" description="Lorem Ipsum is simply Business Industry"/>
    <subscribe-form form-direct="row" class="subscribe-form" btn-desc="subscribe now"/>
    <adress-component/>
  </section>

  <footer-component/>

</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import SectionTitle from './components/SectionTitle.vue';
import RequestForm from './components/RequestForm.vue';
import HeaderSlider from './components/HeaderSliderInFrame.vue';
import GridItem from './components/GridItem.vue';
import HalfPictereHalfColor from './components/HalfPicHalfColor.vue';
import PayCards from './components/PayCards.vue';
import PathComponent from './components/PathComponent.vue';
import CommentsComponent from './components/CommentsComponent.vue';
import SubscribeForm from './components/SubscribeForm.vue';
import AdressComponent from './components/AdressComponent.vue';
import FooterComponent from './components/FooterComponent.vue';

export default {
  data() {
    return {
      headerSliderPics: [
        {src: require('./assets/pics/header-slider-pics/first.jpg'), id: "1"}, 
        {src: require('./assets/pics/header-slider-pics/second.jpg'), id: "2"}, 
        {src: require('./assets/pics/header-slider-pics/third.jpg'), id: "3"},
      ],

      ourServicesList: [
        {
          ico: require("./assets/pics/our-services-icons/clock.png"),
          title: "font-awesom icons",
          desc: "lorem saflak gghai gdkf asdgksg ksadj sakgl ;glia sig hagsg ksdj jsalsadf asdg  asg hsdg jskd skd ggkldg kl;ag",
          id: 1,
          
        },
        {
          ico: require("./assets/pics/our-services-icons/gear.png"),
          title: "font-awesom icons",
          desc: "lorem saflak gghai gdkf asdgksg ksadj sakgl ;glia sig hagsg ksdj jsalsadf asdg  asg hsdg jskd skd ggkldg kl;ag",
          id: 2,
        },
        {
          ico: require("./assets/pics/our-services-icons/hat.png"),
          title: "font-awesom icons",
          desc: "lorem saflak gghai gdkf asdgksg ksadj sakgl ;glia sig hagsg ksdj jsalsadf asdg  asg hsdg jskd skd ggkldg kl;ag",
          id: 3,
        },
        {
          ico: require("./assets/pics/our-services-icons/rocket.png"),
          title: "font-awesom icons",
          desc: "lorem saflak gghai gdkf asdgksg ksadj sakgl ;glia sig hagsg ksdj jsalsadf asdg  asg hsdg jskd skd ggkldg kl;ag",
          id: 4,
        },
        {
          ico: require("./assets/pics/our-services-icons/peace.png"),
          title: "font-awesom icons",
          desc: "lorem saflak gghai gdkf asdgksg ksadj sakgl ;glia sig hagsg ksdj jsalsadf asdg  asg hsdg jskd skd ggkldg kl;ag",
          id: 5,
        },
        {
          ico: require("./assets/pics/our-services-icons/usd.png"),
          title: "font-awesom icons",
          desc: "lorem saflak gghai gdkf asdgksg ksadj sakgl ;glia sig hagsg ksdj jsalsadf asdg  asg hsdg jskd skd ggkldg kl;ag",
          id: 6,
        },
      ],

      halfPicSrc: require("./assets/pics/about-us-section/about-us-pic.jpg"),

      priceCards: [
        {
          id: 1, 
          title: "basic plan", 
          price: 22, 
          recomend: false,
          advanteges: [
            "1 accaunt",
            "8 hour support",
            "custom cloud services"
          ]},
        {
          id: 2, 
          title: "premium plan", 
          price: 42, 
          recomend: true,
          advanteges: [
            "2 accaunts",
            "100mb storage",
            "custom cloud services"
          ]},
        {
          id: 3, 
          title: "basic plan", 
          price: 62, 
          recomend: false,
          advanteges: [
            "8 accaunts",
            "24 hour support",
            "custom cloud services"
          ]},
      ],

      commentsList:[
        {
          id:1,
          description: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Molestiae nihil ullam ipsum ex vero dignissimos earum doloribus error voluptates reiciendis? Nostrum sunt iusto fugiat esse corporis maiores molestiae, quidem odio.",
          userName: "Darvin Michle",
          userFunction: "project manager",
          userPicture: require("./assets/pics/user-img/first-user.jpg"),
        },
        {
          id:2,
          description: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Molestiae nihil ullam ipsum ex vero dignissimos earum doloribus error voluptates reiciendis? Nostrum ",
          userName: "madam elisabeth",
          userFunction: "creative director",
          userPicture: require("./assets/pics/user-img/second-user.jpg"),
        },
        {
          id:3,
          description: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Molestiae nihil ullam ipsum ex vero dignissimos earum doloribus error voluptates reiciendis? Nostrum sunt iusto fugiat esse corporis",
          userName: "clips arter",
          userFunction: "lipsum directer",
          userPicture: require("./assets/pics/user-img/third-user.jpg"),
        },
        {
          id:4,
          description: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Molestiae nihil ullam ipsum ex vero dignissimos earum doloribus error voluptates reiciendis? Nostrum sunt iusto fugiat esse corporis maiores molestiae,",
          userName: "zam cristafer",
          userFunction: "manager",
          userPicture: require("./assets/pics/user-img/fourth-user.jpg"),
        },
      ],
    }
  },
  name: 'App',
  components: {
    HeaderComponent,
    SectionTitle,
    RequestForm,
    HeaderSlider,
    GridItem,
    HalfPictereHalfColor,
    PayCards,
    PathComponent,
    CommentsComponent,
    SubscribeForm,
    AdressComponent,
    FooterComponent,
  }
}
</script>

<style>

/* Paddings and margins start */

.header-title{
  text-align: center;
  padding-top: 110px;
}
.header-form{
  margin-top: 100px;
}
.header-slider{
  margin-top: 67px;
}
.our-services-items{
  margin-bottom: 150px;
}
.our-services-title{
  padding-top: 90px;
  margin-bottom: 95px;
}
.our-price{
  padding: 135px 0 160px;
}
.price-title{
  margin-bottom: 50px;
}
.how-it-work{
  padding-top: 155px;
}
.how-it-work-title{
  margin-bottom: 110px;
}
.comments{
  padding: 140px 0 160px;
}
.comments-title{
  margin-bottom: 60px;
}
.contacts{
  padding-top: 150px;
  padding-bottom: 70px;
}
.contact-title{
  margin-bottom: 40px;
}

/* Paddings and margins end*/

.header-desc{
  background-color: #709dca;
  height: 670px;
  padding-top: 90px;
  margin-bottom: 100px;
}
.container-1170{
    margin: 0 auto;
    max-width: 1200px;
    padding: 0 15px;
}
.our-price{
  background-color: #e7edf3;
}
.comments{
  background-color: #ffc155;
}

@media (max-width: 1200px) {
  .header-desc{
    height: 920px;
  }
}
</style>
