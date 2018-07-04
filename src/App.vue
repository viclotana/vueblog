<template >
  <div id="app" >
  <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
  <a class="navbar-brand" href="#">Adidas.yeezy</a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarColor01" aria-controls="navbarColor01" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>
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
  <div class="container">
    <transition name="moveInUp">
      <router-view/>
    </transition>
  </div>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0px;
}
.moveInUp-enter-active{
  animation: fadeIn 1.8s ease-in;
}
@keyframes fadeIn{
  0%{
    opacity: 0;
  }
  50%{
    opacity: 0.4;
  }
  100%{
    opacity: 0.9;
  }
}
.moveInUp-leave-active{
  animation: moveInUp .2s ease-in;
}
@keyframes moveInUp{
 0%{
  transform: translateY(0);
 }
 50%{
   transform: translateY(-200px);
}
  100%{
  transform: translateY(-400px);
 }
}
</style>
