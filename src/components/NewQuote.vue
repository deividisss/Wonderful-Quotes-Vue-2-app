<template>
  <div class="container">
    <div class="row">
      <app-quote style="margin: 0 auto" :quote="quote"></app-quote>
    </div>

    <form class="mt-4" @submit.prevent="addNewQuote">
      <div class="form-group">
        <label for="comment">Quote text:</label>
        <!-- <textarea class="form-control" rows="5" id="comment" name="text" v-model="quote"></textarea> -->
        <input
          id="comment"
          v-model="quote.quote"
          class="form-control"
          name="text"
        />
      </div>
      <div class="form-group">
        <label for="author">Author:</label>
        <input
          id="author"
          v-model="quote.author"
          class="form-control"
          name="text"
        />
      </div>
      <div class="text-center">
        <button
          type="submit"
          class="btn btn-success btn-lg mt-2"
          :disabled="isButtonDisabled"
        >
          Add Quote
        </button>
        <!-- <button @submit.prevent>SFfsfsf</button> -->
      </div>
    </form>
  </div>
</template>

<script>
import appQuote from "./../components/Quote.vue";

export default {
  components: {
    appQuote
  },
  props: ["quotes", "quotesCount"],
  data() {
    return {
      btnDisabled: false,
      quote: {
        quote: null,
        author: null
      }
    };
  },
  computed: {
    isButtonDisabled() {
      if (this.quotesCount >= 10) {
        return true;
      } else {
        return false;
      }
    }
  },
  methods: {
    addNewQuote() {
      if (this.quotesCount >= 10) {
        alert("Quotes limit reached");
      } else {
        if (!this.quote.quote) {
          alert("Quote text empty ad some text");
        } else {
          this.quotes.unshift({
            quote: this.quote.quote,
            author: this.quote.author
          });
          this.quote.quote = null;
          this.quote.author = null;
          let myNumber = this.quotesCount;
          myNumber++;
          this.$emit("update-count", myNumber);
        }
      }
    },
    daugiau() {
      this.quotesCount++;
    }
  }
};
</script>
