<script setup>
import AddFooter from './components/AppFooter.vue';
import AddHeader from './components/AppHeader.vue';

</script>

<template>
  <AddHeader />
  <main class="container py-5">
    <RouterView />
  </main>
  <AddFooter />
</template>

<style lang="scss" scoped>
main {
  margin-top: 56px;
  margin-bottom: 40px;
}
</style>
