<template>
  <nav id="headerSection" class="navbar navbar-expand-lg">
  <div class="container-fluid">
    <img src="../../public/favicon.png" alt="iconPerson">
    <a id="headerSection-name" class="navbar-brand" href="#">Cala.Code</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <a class="nav-link" href="#">Participantes</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Premios</a>
        </li>
        <li class="nav-item dropdown">
          <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-bs-toggle="dropdown" aria-expanded="false">
            Ciudades
          </a>
          <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
            <li><a class="dropdown-item" href="#">Bogotá</a></li>
            <li><a class="dropdown-item" href="#">Medellín</a></li>
            <li><a class="dropdown-item" href="#">Cali</a></li>
          </ul>
        </li>
      </ul>
      <form class="d-flex" role="search">
        <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
        <button id="headerSection-buttonSearch" class="btn btn-outline-success" type="submit">Go</button>
      </form>
    </div>
  </div>
</nav>
</template>

<style scoped>
  #headerSection{
    background-color: #0da2a5;
    border-radius: 25px;
    padding: 5px;
    color: #d9eeef;
  }
  img{
    width: 50px;
    height: 50px;
  }
  #headerSection-name{
    color: #d9eeef;
    font-size: x-large;
  }
  #headerSection-buttonSearch{
    background-color: #67c9cb;
    color: #d9eeef;
  }
</style>