
<template>

<main  class=" d-flex flex-column mt-5 justify-content-center align-items-center pt-3 pb-3 ">
  
  <form action="" class="rounded bg-light w-50 shadow-lg pt-3 pb-3 align-items-center">

    <h3 class="pt-4 pb-3">Faça seu Login:</h3>
    <div class=" d-flex flex-rown p-3 m-2">
    <label for="formGroupExampleInput" class="form-label  p-2">Email:</label>
    <input type="text" class="form-control shadow-sm" id="formGroupExampleInput" placeholder="name@example.com">
  </div>
  <div class=" d-flex flex-rown p-3 m-2">
    <label for="formGroupExampleInput2" class="form-label p-2 ">Senha:</label>
    <input type="text" class="form-control shadow-sm " id="formGroupExampleInput2" placeholder="Senha">
  
  </div>
  <button type="submit" class="btn btn-outline-primary p-2 mb-3">Fazer Login</button>

  <p>Não tem uma conta?<router-link to="/Register">Registre-se</router-link></p>
</form>
</main>

</template>

<style>

body{

  backdrop-filter: blur(5px);
  background-color: rgb(22, 71, 116);
}
</style>