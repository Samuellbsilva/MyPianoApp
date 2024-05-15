<template>


<nav class="navbar border-bottom border-body" data-bs-theme="dark">
   
    
    <div class="container-fluid justify-content-center">
      <router-link v-if="isHomePage" to="/">
        <span class="navbar-brand">MyPiano</span>
      </router-link>
      <router-link v-if="isHomePage !== true" to="/">
        <img src="../assets/icons8-electronic-music-64.png" alt="">
      </router-link>
    
        <ul v-if="isHomePage === true" class="navbar-nav flex-row">
          <li class="nav-item m-2">
            <router-link to="/Login" class="btn btn-outline-primary">Login</router-link>
          </li>
          <li class="nav-item m-2">
            <router-link to="/Register" class="btn btn-outline-primary">Registro</router-link>
          </li>
        </ul>
    </div>
   
    
  
</nav>

</template>


<script>
export default {
  computed: {
    isHomePage() {
      return this.$route.path === '/';
    },
    }
}
</script>

<style scoped>
@keyframes gradient {
  0% { background-position: 0% 50% }
  50% { background-position: 100% 50% }
  100% { background-position: 0% 50% }
}

nav {
  background: linear-gradient(90deg, rgba(2,0,36,1) 0%, rgb(40, 40, 42) 35%, rgb(0, 0, 0) 100%);
  background-size: 400% 400%;
  animation: gradient 8s linear infinite;
}

/* Remove underline from Bootstrap links globally */
* {
  text-decoration: none !important;
}
</style>
