
<template>
    

    <nav class="navbar  border-bottom border-body" data-bs-theme="dark">

  <div class="container-fluid justify-content-center">
    <a v-if="isNotHomePage" class="navbar-brand" href=""><router-link to="/">MyPiano</router-link></a>
    

 | <ul v-if="isNotHomePage" class="navbar-nav flex-row">
    <li class="nav-item m-2">
         
        <button type="button" class="btn btn-outline-primary"><router-link to="/Login">Login</router-link></button>
        </li>
        <li class="nav-item m-2">

          <button type="button" class="btn btn-outline-primary"><router-link to="/Register">Registro</router-link></button>

        </li>
    </ul>
  </div>
</nav>

  </template>


<script>
export default {
  computed: {
    isNotHomePage() {
      
      return this.$route.path !== '/Login' && this.$route.path !== '/Register';
    },
    isHomePage() {
      
      return this.$route.path ==='/Login' && this.$route.path === '/Register';
    }
},


}
</script>
<style>
    @keyframes gradient {
    0%{background-position:0% 50%}
    50%{background-position:100% 50%}
    100%{background-position:0% 50%}
}
  
nav{
 
      background: linear-gradient(90deg, rgba(2,0,36,1) 0%, rgb(40, 40, 42) 35%, rgb(0, 0, 0) 100%);
  background-size: 400% 400%;
  animation: gradient 8s linear infinite;
  
}
/* Remove underline from Bootstrap links globally */
*{
  text-decoration: none !important;
}
</style>
