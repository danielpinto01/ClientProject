<template>
  <div id="app">
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/register">Registro</router-link>
    </div>-->

    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <a class="navbar-brand" href="/">CovidApp</a>
      <!-- <button
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button> -->
      <!-- <div class="collapse navbar-collapse" id="navbarNav"> -->
      <div id="navbarNav">
        <ul class="navbar-nav">
          <!-- <li class="nav-item active">
            <a class="nav-link" href="/">
              Inicio
              <span class="sr-only">(current)</span>
            </a>
          </li> -->
          <li class="nav-item">
            <a class="nav-link" href="#/register">Registro</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#/list">Lista</a>
          </li>
           <li class="nav-item">
            <a class="nav-link" href="#/graphic">Grafico</a>
          </li>
           <li class="nav-item">
            <a class="nav-link" href="#/monitoring">Monitoreo</a>
          </li>
        </ul>
      </div>
    </nav>

    <router-view />
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
