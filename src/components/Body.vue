<template>
  <div class="container">
    <div class="row">
      <div class="col">
        <h4>Ganaradores del concurso VIP</h4>
        <UserList></UserList>
      </div>
    </div>
  </div>
</template>

<script setup>
  import UserList from './UserList.vue';
</script>

<style scoped>
  h4{
    text-align: center;
    color: #03888f;
    background-color: #d9eeef;
    font-size: xx-large;
    margin-top: 20px;
    margin-bottom: 20px;
    padding-top: 10px;
    padding-bottom: 10px;
    border-radius: 30px;
  }
</style>