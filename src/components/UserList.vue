<template>
<div class="container">
  <div class="row">
    <div class="col-12">
      <input class="d-flex justify-content-center" id="inputSearch" placeholder="Buscar por nombre" type="text" v-model="search">
    </div>
  </div>
  <div class="row">
    <div class="col-4" v-for="user in filteredUsers" :key="user.id">
      <div class="card" style="width: 18rem;">
        <div class="card-body">
          <h3 class="card-title">{{ user.name }}</h3>
          <p class="card-text">Ganador@ de la ciudad de <b>{{ user.address.city }}</b></p>
          <!-- <a href="#" class="btn btn-primary">+ Info</a> -->
          <p>
            <button class="btn btn-primary" type="button" data-bs-toggle="collapse" data-bs-target="#collapseWidthExample" aria-expanded="false">
              + Info
            </button>
          </p>
          <div style="min-height: 120px;">
            <div class="collapse collapse-horizontal" id="collapseWidthExample">
              <div class="card card-body" style="width: 16rem;">
                {{ user.name }}
                <b>Email:</b>{{ user.email }}
                <b>Phone:</b>{{ user.phone }}
                <b>Web:</b>{{ user.website }}
                <b>Company:</b>{{ user.company.name }}
              </div>
            </div>
          </div>

          
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
        search: '',
        users: [],
      };
    },
    computed: {
      filteredUsers(){
        return this.users.filter(user => user.name.toLowerCase().includes(this.search.toLowerCase()))
      }
    },

    async created() {
      let url = "https://jsonplaceholder.typicode.com/users";

      await axios.get(url).then((resultado) => (this.users = resultado.data));
    },
  };
</script>

<style scoped>
  #inputSearch{
    border-radius: 25px;
    margin: 10px;
  }
</style>