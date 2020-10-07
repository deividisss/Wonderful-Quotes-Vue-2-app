<template>
  <div class="row">
    <!-- <div class="row bg-primary text-light"> -->
    <app-quote
      v-for="(quote, index) in quotes"
      :key="index + quote.author"
      :quote="quote"
      :index="index"
      :hover="hover"
      @delete-quote="remove($event)"
      :mode="mode"
    ></app-quote>
  </div>
</template>

<script>
import appQuote from "./../components/Quote.vue";

export default {
  components: {
    appQuote,
  },
  props: ["quotes", "hover", "mode"],
  methods: {
    remove(index) {
      if (this.mode === "edit") {
        this.$delete(this.quotes, index);
      }
    },
  },

  created() {
console.log("Hello from JS!");
 console.log('The time is ' . this.$moment().format("HH:mm"));
  },
};
</script>