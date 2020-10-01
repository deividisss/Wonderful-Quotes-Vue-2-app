<template>
  <div class="container mb-4">
    <p class="display-4 pt-1">Quotes Added</p>
    <div class="progress" style="height: 1.5rem">
      <div
        class="progress-bar progress-bar-striped bg-success progress-bar-animated"
        role="progressbar"
        aria-valuenow="75"
        aria-valuemin="0"
        aria-valuemax="100"
        :style="{ width: barWidth + '%' }"
      >
        <span v-if="quotesCount" class="font-weight-bold">
          {{ this.quotesCount }}
          <span>/ 10</span></span
        >
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["quotesCount"],
  data() {
    return {
      kaskas: 1,
    };
  },
  computed: {
    barWidth() {
      return this.quotesCount * 10;
    },
  },
};
</script>

<style scoped>
.progress {
  font-size: 1rem;
}
</style> 