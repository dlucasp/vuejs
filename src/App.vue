<template>
  <div id="app">
    <!-- navbar -->
    <div class="navbar navbar-expand-lg fixed-top navbar-dark fluid-container header">
      <div class="container">
        <router-link to="/" class="navbar-brand">Home</router-link>
        <button
          class="navbar-toggler"
          type="button"
          data-toggle="collapse"
          data-target="#navbarResponsive"
          aria-controls="navbarResponsive"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarResponsive">
          <ul class="navbar-nav">
            <li class="nav-item">
              <router-link class="nav-link" to="/blog">Blog</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" to="/contact">Contato</router-link>
            </li>
          </ul>
        </div>
      </div>
    </div>
    <div class="container">
      <transition name="moveInUp">
        <router-view/>
      </transition>
    </div>

    <!-- footer -->
    <div>
      <div class="fluid-container footer fixed-bottom">
        <div class="elemento">
          <table>
            <tr>
              <td>Matriz</td>
              <td>Filial Cuiába</td>
            </tr>
            <tr>
              <td>
                <p>BR 277, Km 454</p>
                <p>Trevo - CEP 85.301-000</p>
                <p>
                  Laranjeiras do Sul/PR - Brasil
                  Fone: (42) 3635 - 1564
                </p>
              </td>
              <td>
                <p>Av. Carmindo de Campos, 2619</p>
                <p>Bairro Dom Aquino - CEP 78.015-020</p>
                <p>
                  Cuiába/MT - Brasil
                  Fone: (65) 3634 - 3025
                </p>
              </td>
            </tr>
          </table>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App"
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.moveInUp-enter-active {
  animation: fadeIn 2s ease-in;
}
@keyframes fadeIn {
  0% {
    opacity: 0;
  }
  50% {
    opacity: 0.5;
  }
  100% {
    opacity: 1;
  }
}

.moveInUp-leave-active {
  animation: moveInUp 0.3s ease-in;
}
@keyframes moveInUp {
  0% {
    transform: translateY(0);
  }
  100% {
    transform: translateY(-400px);
  }
}

.fluid-container.footer {
  background: #363636;
  color: #fff;
}
.elemento {
  margin: 0 auto;
  width: 40%;
}

.fluid-container.header {
  background: #cd3333;
}
</style>
