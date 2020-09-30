<template>
  <div class="container">
    <div class="row">
      <app-quote
        style="margin: 0 auto"
        :quote="quote"
        :hover="false"
      ></app-quote>
    </div>

    <form @submit.prevent="addNewQuote" class="mt-4">
      <div class="form-group">
        <label for="comment">Quote text:</label>
        <!-- <textarea class="form-control" rows="5" id="comment" name="text" v-model="quote"></textarea> -->
        <input
          class="form-control"
          id="comment"
          name="text"
          v-model="quote.quote"
        />
      </div>
      <div class="form-group">
        <label for="author">Author:</label>
        <input
          class="form-control"
          name="text"
          id="author"
          v-model="quote.author"
        />
      </div>
      <div class="text-center">
        <button type="submit" class="btn btn-success btn-lg mt-2">
          Add Quote
        </button>
      </div>
    </form>
  </div>
</template>

<script>
import appQuote from "./../components/Quote.vue";

export default {
  components: {
    appQuote,
  },
  props: ["quotes", "quotesCount"],
  data() {
    return {
      quote: {
        quote: null,
        author: null,
      },
    };
  },
  methods: {
    addNewQuote() {
      this.quotes.unshift({
        quote: this.quote.quote,
        author: this.quote.author,
      });
      this.quote.quote = null;
      this.quote.author = null;
      let myNumber = this.quotesCount;
      myNumber++;
      this.$emit("update-count", myNumber);
    },
    daugiau() {
      this.quotesCount++;
    },
  },
  computed: {
    skaicius() {
      return this.quotesCount;
    },
  },
};
</script>