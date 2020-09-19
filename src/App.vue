<template>
  <div>
    <div class="jumbotron">
      <div class="container">
        <h1 class="display-4">Wonderfull Quotes</h1>
      </div>
    </div>

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
import appQuote from "./components/Quote.vue";

export default {
  components: {
    appQuote,
  },
};
</script>

<style>
</style>
