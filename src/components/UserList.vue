<template>
<div class="container">
  <div class="row">
    <div class="col-4" v-for="user in users" :key="user.id">
      <div class="card" style="width: 18rem;">
        <div class="card-body">
          <h3 class="card-title">{{ user.username }} {{ user.name }}</h3>
          <p class="card-text">Ganador@ de la ciudad de <b>{{ user.address.city }}</b></p>
          <a href="#" class="btn btn-primary">+ Info</a>
        </div>
      </div>
    </div>
  </div>
</div>
  <div>
    
  </div>
</template>

<script>
  

  export default {
    name: "UserList",

    data() {
      return {
        users: [],
      };
    },

    async created() {
      let url = "https://jsonplaceholder.typicode.com/users";

      await axios.get(url).then((resultado) => (this.users = resultado.data));
    },
  };
</script>

<style scoped>

</style>