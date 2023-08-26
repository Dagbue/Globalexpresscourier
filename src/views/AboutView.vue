<template>
  <div class="about">
    <br/>
    <about-header/>
    <our-values/>
    <we-are/>
    <about-partners/>
    <our-mission/>
    <!--    <dedicated-team/>-->
    <br/>
    <br/>
    <br/>
    <news-letter/>
    <footer-home/>
  </div>
</template>
<script>

import AboutHeader from "@/components/About/About-header";
import OurValues from "@/components/About/Our-Values";
import WeAre from "@/components/About/we-are";
import AboutPartners from "@/components/About/about-partners";
import OurMission from "@/components/About/our-mission";
import NewsLetter from "@/components/Home/news-letter";
import FooterHome from "@/components/Home/footer-home";

export default {
  name: 'AboutView',
  components: {
    FooterHome,
    NewsLetter,
    OurMission,
    AboutPartners,
    WeAre,
    OurValues,
    AboutHeader
  }
}
</script>
<style scoped>

.about{
  margin-right: 0;
  padding-right: 0;
}

</style>