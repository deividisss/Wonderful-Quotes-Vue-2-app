<template>
  <div class="col-sm-4 mt-4">
    <div class="border p-4" @click="$emit('delete-quote', index)">
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
  methods: {},
  created() {},
};
</script>