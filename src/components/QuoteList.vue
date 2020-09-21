<template>
  <div class="row">
    <!-- <div class="row bg-primary text-light"> -->
    <app-quote v-for="(quote, index) in quotes" :key="index + author" :quote="quote"></app-quote>
  </div>
</template>

<script>
import appQuote from "./../components/Quote.vue";

export default {
  components: {
    appQuote,
  },
  props: ["quotes"],

  created() {},
};
</script>