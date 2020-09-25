<template>
  <div class="container">
    <div class="row">
      <app-quote style="margin: 0 auto" :quote="quote"></app-quote>
    </div>

    <form @submit.prevent="onSubmit" class="mt-4">
      <div class="form-group">
        <label for="comment">Quote text:</label>
        <!-- <textarea class="form-control" rows="5" id="comment" name="text" v-model="quote"></textarea> -->
        <input class="form-control" id="comment" name="text" v-model="quote.quote" />
      </div>
      <div class="form-group">
        <label for="author">Author:</label>
        <input class="form-control" name="text" id="author" v-model="quote.author" />
      </div>
      <div class="text-center">
        <button type="submit" class="btn btn-success btn-lg mt-2">Add Quote</button>
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
  data() {
    return {
      quote: {
        quote: null,
        author: null,
      },
    };
  },
  methods: {
    onSubmit(e) {
      alert(this.quote.quote + this.quote.author);
    },
  },
};
</script>