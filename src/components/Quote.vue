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
        <p class="mb-0">{{ quote.quote }}</p>
        <footer class="blockquote-footer">
          Written by
          <cite :title="quote.author">{{quote.author}}</cite>
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
    return {};
  },
  computed: {
    activeHover() {
      if (this.hover === undefined) {
        return (this.hover = true);
      }
    },
  },
};
</script>

<style scoped>
.quote:hover {
  cursor: pointer;
  background-color: rgb(255 87 104 / 30%);
}
</style>