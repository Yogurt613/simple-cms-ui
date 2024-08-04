<script setup>
defineProps({
  msg: {
    type: String,
    default: '',
  },
});
</script>

<template>
  <button
    type="button"
    class="btn btn-primary"
  >
    {{ msg }}
  </button>
</template>

<style scoped>

</style>
