<template>
  <div class="col-sm-4 mt-4">
    <div class="border p-4">
      <!-- <div class="border p-4" @click="deleteQuote"> -->
      <h4>Quote</h4>
      <p>{{ quote.quote }}</p>
      <p>
        <i>
          <b>Author:</b>
          {{quote.author}}
        </i>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  props: ["quote", "index"],
  methods: {
    deleteQuote() {
      this.quote.author = this.index;
    },
  },
  created() {
    console.log(this.quote);
  },
};
</script>