<template>
  <div id="app">
   <nav class="navbar navbar-expand-lg navbar-dark bg-primary">


  <div class="collapse navbar-collapse" id="navbarColor01">
    <ul class="navbar-nav mr-auto">
      <li class="nav-item active">
   <router-link class="nav-link" to="/">Home</router-link>
      </li>
      <li class="nav-item">
  <router-link class="nav-link" to="/blog">Blog</router-link>
      </li>
      <li class="nav-item">
  <router-link class="nav-link" to="/services">Services</router-link>
      </li>
      <li class="nav-item">
   <router-link class="nav-link" to="/contact">Contact</router-link>
      </li>
    </ul>
   
  </div>
</nav>
    
<transition name="moveInUp" >
         <router-view/>
  </transition>  </div>
</template>
<script>
export default {
  name: 'App',
};
</script>
<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 25px;
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
</style>
