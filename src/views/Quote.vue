<template>
<div>
  <br/>
  <quote-header/>
  <quote-body/>
  <news-letter/>
  <footer-home/>
</div>
</template>

<script>
import QuoteHeader from "@/components/Quote/quote-header";
import QuoteBody from "@/components/Quote/quote-body";
import NewsLetter from "@/components/Home/news-letter";
import FooterHome from "@/components/Home/footer-home";
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Quote",
  components: {FooterHome, NewsLetter, QuoteBody, QuoteHeader}
}
</script>

<style scoped>

</style>