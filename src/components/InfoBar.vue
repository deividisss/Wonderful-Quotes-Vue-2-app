<template>
  <div v-show="showBar" class="row">
    <div class="col mt-4 text-center">
      <div class="alert alert-primary" role="alert">
        <slot></slot>
        <button
          type="button"
          class="close"
          aria-label="Close"
          @click="showBar = false"
        >
          <span aria-hidden="true">&times;</span>
        </button>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      showBar: true
    };
  }
};
</script>
