<template>
  <div class="row">
    <!-- <div class="row bg-primary text-light"> -->
    <app-quote v-for="index in 10" :key="index"></app-quote>
  </div>
</template>

<script>
import appQuote from "./../components/Quote.vue";

export default {
  components: {
    appQuote,
  },
};
</script>