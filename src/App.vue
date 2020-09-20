<template>
  <div>
    <app-header>
      <slot>{{ name }}</slot>
    </app-header>
    <div class="container">
      <div class="row bg-primary text-light">
        <app-quote></app-quote>
        <app-quote></app-quote>
        <app-quote></app-quote>
        <app-quote></app-quote>
        <app-quote></app-quote>
        <app-quote></app-quote>
        <app-quote></app-quote>
        <app-quote></app-quote>
      </div>
    </div>
  </div>
</template>

<script>
// Quote wall Limit 10
// Tweet quote
// Fetch Quote
// Quote Design pagal temą
// Local storage

import appQuote from "./components/Quote.vue";
import appHeader from "./components/layout/Header.vue";

export default {
  components: {
    appQuote,
    appHeader,
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

