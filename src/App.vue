<template>
  <div>
    <app-header>
      <slot>{{ name }}</slot>
    </app-header>
    <div class="container">
      <app-quote-list></app-quote-list>
    </div>
  </div>
</template>

<script>
// Alert box kuris saka istrink quotes, jei nori pridėt
// Quote wall Limit 10
// Tweet quote
// Fetch Quote
// Quote Design pagal temą
// Local storage

import appHeader from "./components/layout/Header.vue";
import appQuote from "./components/Quote.vue";
import appQuoteList from "./components/QuoteList.vue";

export default {
  components: {
    appQuote,
    appHeader,
    appQuoteList,
  },
  data() {
    return {
      name: "Wonderfull Quotes",
    };
  },
};
</script>

<style>
</style>

