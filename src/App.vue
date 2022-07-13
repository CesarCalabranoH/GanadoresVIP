<template>
  <mainHeader></mainHeader>
  <mainBody></mainBody>
  <mainFooter></mainFooter>
</template>

<script setup>
import mainHeader from './components/Header.vue';
import mainBody from './components/Body.vue'
import mainFooter from './components/Footer.vue';
</script>

<style>
@import './assets/base.css';
#app{
  padding: 20px;
}
</style>
