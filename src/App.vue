<script setup>
import AddFooter from './components/AppFooter.vue';
import AddHeader from './components/AppHeader.vue';
import HelloWorld from './components/HelloWorld.vue';

</script>

<template>
  <AddHeader />
  <main class="container py-5">
    <HelloWorld msg="Hello, World!" />
  </main>
  <AddFooter />
</template>

<style lang="scss" scoped>
main {
  margin-top: 56px;
  margin-bottom: 40px;
}
</style>
