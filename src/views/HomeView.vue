<template>
  <div class="home">
    <Slider/>
    <about-company/>
    <partners-home/>
    <trusted/>
    <client-review/>
    <latest-news/>
    <special/>
    <not-sure/>
    <contact-now/>
    <news-letter/>
    <footer-home/>
  </div>
</template>

<script>
import Slider from "@/components/Home/slideshow/Slider";
import AboutCompany from "@/components/Home/about-company";
import PartnersHome from "@/components/Home/partners-home";
import Trusted from "@/components/Home/Trusted";
import ClientReview from "@/components/Home/client-review";
import LatestNews from "@/components/Home/latest-news";
import Special from "@/components/Home/Special";
import NotSure from "@/components/Home/not-sure";
import ContactNow from "@/components/Home/contact-now";
import NewsLetter from "@/components/Home/news-letter";
import FooterHome from "@/components/Home/footer-home";
export default {
  name: 'HomeView',
  components: {
    FooterHome,
    NewsLetter,
    ContactNow,
    NotSure,
    Special,
    LatestNews,
    ClientReview,
    Trusted,
    PartnersHome,
    AboutCompany,
    Slider
  },
}
</script>
