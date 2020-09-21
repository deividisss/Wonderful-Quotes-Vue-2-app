<template>
  <div class="row">
    <!-- <div class="row bg-primary text-light"> -->
    <app-quote
      v-for="(quote, index) in quotes"
      :key="index"
      :quote="quote"
      :index="index"
      @click.native="$delete(quotes, index)"
    ></app-quote>
  </div>
</template>

<script>
import appQuote from "./../components/Quote.vue";

export default {
  components: {
    appQuote,
  },
  props: ["quotes"],
  methods: {
    // deleteEvent: function (index) {
    //   this.quotes.splice(index, 1);
    // },
  },

  created() {},
};
</script>