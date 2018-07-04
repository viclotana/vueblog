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
    <transition name="moveInUp">
      <router-view/>
    </transition>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
</style>
