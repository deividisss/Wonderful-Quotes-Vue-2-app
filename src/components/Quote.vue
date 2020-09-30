<template>
  <div class="col-lg-4 mt-4">
    <div
      class="border rounded p-4"
      @click="$emit('delete-quote', index)"
      :class="{ quote: activeHover }"
    >
      <!-- <div class="border p-4" @click="deleteQuote"> -->
      <h4>Quote</h4>

      <blockquote class="blockquote">
        <p class="mb-0 quote-text">{{ quote.quote }}</p>
        <footer class="blockquote-footer">
          Written by
          <cite :title="quote.author">{{ quote.author }}</cite>
        </footer>
      </blockquote>
    </div>
  </div>
</template>

<script>
export default {
  props: ["quote", "index", "hover"],
  methods: {},
  created() {},
  data() {
    return {
      whiteShow: true,
    };
  },
  computed: {
    activeHover() {
      if (this.hover === undefined) {
        return (this.hover = true);
      }
    },
    // quoteText() {
    //   if (this.quote.quote === null || this.quote.quote === "") {
    //     return "&nbsp;";
    //   } else {
    //     return this.quote.quote;
    //   }
    // },
  },
  watch: {
    // "quote.quote"() {
    //   if (this.quote.quote === null || this.quote.quote === "") {
    //     this.whiteShow = true;
    //   } else {
    //     this.whiteShow = false;
    //   }
    // },
  },
};
</script>

<style scoped>
.quote:hover {
  cursor: pointer;
  background-color: rgb(255 87 104 / 30%);
}
</style>