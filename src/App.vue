<template>
  <div class="container">
    <div class="wrapper">
      <WishList />
    </div>
    <FormCreate />
  </div>
</template>

<script setup>
import FormCreate from './components/FormCreate.vue'
import WishList from './components/WishList.vue'
</script>

<style scope>
@import './assets/global.css';
@import './assets/card.css';
@import './assets/form.css';
</style>
