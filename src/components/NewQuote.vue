<template>
  <form @submit.prevent="onSubmit" class>
    <h2>Quote</h2>
    <div class="form-group">
      <label for="comment">Quote text:</label>
      <!-- <textarea class="form-control" rows="5" id="comment" name="text" v-model="quote"></textarea> -->
      <input class="form-control" id="comment" name="text" v-model="quote" />
    </div>
    <div class="form-group">
      <label for="author">Author:</label>
      <input class="form-control" name="text" id="author" v-model="author" />
    </div>
    <!-- <p>{{ quote }}</p> -->
    <button type="submit" class="btn btn-success btn-lg mt-2">Add Quote</button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      quote: null,
      author: null,
    };
  },
  methods: {
    onSubmit(e) {
      alert(this.quote + this.author);
    },
  },
};
</script>