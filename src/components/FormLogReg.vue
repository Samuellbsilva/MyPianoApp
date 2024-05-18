<template>

    <main  class=" d-flex flex-column mt-5 justify-content-center align-items-center pt-3 pb-3 ">
      
      <form  action="" class="background w-50 shadow-lg pt-3 pb-3 align-items-center rounded">
    
        <h3 class="pt-4 pb-3 text-ligth">{{ FormMsg }}</h3>

        <div v-if="this.$route.path === '/Register'" class=" d-flex flex-rown p-3 m-2">
        <label for="formGroupExampleInput" class="form-label  p-2 text-ligth">Nome:</label>
        <input type="text" class="form-control shadow-sm" id="formGroupExampleInput" placeholder="Seu nome">
      </div>
      <div class=" d-flex flex-rown p-3 m-2">
        <label for="formGroupExampleInput" class="form-label  p-2 text-ligth">Email:</label>
        <input type="text" class="form-control shadow-sm" id="formGroupExampleInput" placeholder="name@example.com">
      </div>
      <div class=" d-flex flex-rown p-3 m-2">
        <label for="formGroupExampleInput2" class="form-label p-2 text-ligth">Senha:</label>
        <input type="text" class="form-control shadow-sm " id="formGroupExampleInput2" placeholder="Senha">
      
      </div>
      <button type="submit" class="btn btn-outline-primary p-2 mb-3 text-ligth">{{ FormMsg }}</button>
    
      <p>{{ ForMsgn }}<router-link v-bind:to="FixRoute">{{ FormMsgReverse }}</router-link></p>
    </form>
    </main>
    
    </template>
    
    <style>
  
    @keyframes gradient {
      0%{background-position:0% 50%}
      50%{background-position:100% 50%}
      100%{background-position:0% 50%}
  }
    body{
      background: linear-gradient(90deg, rgb(4, 1, 64) 0%, rgb(6, 6, 161) 35%, rgb(0, 0, 0) 100%);
    background-size: 400% 400%;
    animation: gradient 8s linear infinite;
    
    }
    .background{
      background: linear-gradient(90deg, rgb(13, 5, 171) 0%, rgb(6, 6, 161) 35%, rgb(2, 2, 102) 100%);
color:aliceblue;
-webkit-backdrop-filter: blur(30px)!important;
        backdrop-filter: blur(30px)!important;
}
 

    
    </style>
    <script>



export default {
  computed: {

    FixRoute() {
      if (this.$route.path === '/Login') {
        return '/Register';
      } else if (this.$route.path === '/Register') {
        return '/Login';
      }
    },
    FormMsg() {
        
    
    if(this.$route.path === '/Login' ){

        return 'Faça seu Login';
  }
  else if (this.$route.path === '/Register'){

 return 'Registre-se';
  }
  },
  FormMsgReverse() {
        
    
        if(this.$route.path === '/Login' ){
    
            return 'Registre-se';
      }
      else if (this.$route.path === '/Register'){
    
     return 'Faça seu Login';
      }
      },
  ForMsgn() {
        
    
        if( this.$route.path === '/Login' ){
    
            return 'Não tem uma conta?';
      }
      else if (this.$route.path === '/Register'){
    
     return 'Já tem uma conta?';
      }
    }
}


}

</script>