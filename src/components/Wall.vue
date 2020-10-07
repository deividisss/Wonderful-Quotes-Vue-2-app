<template>
  <div class="container-fluid text-center my-4">
    <h1 class="display-4 mb-4">Personal Quotes Wall</h1>
    <div class="box p-4 -4">
      <app-quote-list :quotes="quotes" mode="display"></app-quote-list>
    </div>
  </div>
</template>

<script>
import appQuoteList from ".././components/QuoteList.vue";

export default {
  components: {
    appQuoteList
  },
  props: ["quotes"]
};
</script>
<style scoped>
.box {
  box-shadow: 0 2.8px 2.2px rgba(0, 0, 0, 0.034),
    0 6.7px 5.3px rgba(0, 0, 0, 0.048), 0 12.5px 10px rgba(0, 0, 0, 0.06),
    0 22.3px 17.9px rgba(0, 0, 0, 0.072), 0 41.8px 33.4px rgba(0, 0, 0, 0.086),
    0 100px 80px rgba(0, 0, 0, 0.12);

  min-height: 600px;
  width: 90vw;
  margin: 0px auto;
  background: white;
  border-radius: 5px;
}

body {
  background: #eef2f7;
}
</style>
