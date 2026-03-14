<script setup>
  import { ref } from 'vue'
  import EmployeePage from './components/Layout/EmployeePage.vue'
  import HomePage from './components/Layout/HomePage.vue'

  const isHome = ref(true);
  const isEmployeePage = ref(false);
</script>
<template>
  <div id="app">
    <div v-if="isHome">
      <HomePage />
    </div>
    <div v-else-if="isEmployeePage">
      <EmployeePage />
  </div>
</div>
</template>

<style scoped>

</style>
