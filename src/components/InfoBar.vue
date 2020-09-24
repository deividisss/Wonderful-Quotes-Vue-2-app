<template>
  <div class="row" v-show="showBar">
    <div class="col mt-4 text-center">
      <div class="alert alert-primary" role="alert">
        <slot></slot>
        <button @click="showBar = false" type="button" class="close" aria-label="Close">
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
      showBar: true,
    };
  },
};
</script>