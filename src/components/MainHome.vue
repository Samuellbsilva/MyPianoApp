<template>
  <main class="d-flex flex-column h-100 w-100 pl-3 pr-3 pb-5 pt-2">
    <h1 class=" display-1 txt1 pt-3 pb-3 mb-3 align-items-end "><strong>MyPiano</strong></h1>
    <div class="d-flex flex-rown p-2 justify-content-center align-content-center">
     
      <div class="d-flex w-50 justify-content-center">
        <img class="w-100 h-100 concerttransform" src="../assets/MainPicture.png" alt="">
      </div>
      <div class="d-flex w-50  flex-column justify-content-center align-content-center align-content-center">
        <h2 class="txt display-2"><strong>Aprenda Piano sem <span v-bind:style="colorStyle">{{ currentText }}</span></strong></h2>
        <h3 class="txt">A melhor plataforma para virar um verdadeiro pianista</h3>
      </div>
    </div>
    <div class="mt-3 d-flex justify-content-center">
    <router-link to="/Register" class="w-25 btn btn-outline-primary p-2 mb-3 ">Inicie agora</router-link>
  </div>
  </main>
  </template>
  
  <script>
  export default {
    data() {
      return {
        currentText: 'estresse!',
        colorStyle: { color: 'white' } 
    };
  },
  methods: {
    change() {
      const texts = ['estresse!', 'chatices!', 'problema!'];
      const colors = ['#1E90FF', '#4169E1', '#6495ED'];

      
      const randomIndex = Math.floor(Math.random() * texts.length);
      
      this.colorStyle.color = colors[randomIndex]; 
      this.currentText = texts[randomIndex];
    },

  },
    mounted() {
      this.change(); 
      setInterval(this.change, 2000); 
    }
  };
  </script>
  
  <style>
 
  .txt {
    color: white;
    font-family: Helvetica;
  }
 
  @keyframes titleAnimation {
  0% {
    transform: scale(1.5);
    opacity: 0;
  }
  100% {
    transform: scale(1);
    opacity: 1;
  }
}

.txt1 {
  font-family: 'Playfair Display', serif;
  
  color: #ffffff;
  animation: titleAnimation 1s ease-out forwards;
}

  .concerttransform:hover {
    transform: scale(1.0);
  }
  main{
    opacity: 0;
  animation: fadeInAnimation 2s ease forwards;
  }

@keyframes fadeInAnimation {
  0% {
    opacity: 0;
    transform: translateY(40px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
} 
  
  </style>
  