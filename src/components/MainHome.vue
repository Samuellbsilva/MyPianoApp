<template>
    <main class="d-flex h-100 w-100 flex-rown">
      <div></div>
      <div class="d-flex w-50 justify-content-center align-items-center">
        <img class="w-100 concerttransform" src="../assets/MainPicture.png" alt="">
      </div>
      <div class="d-flex w-50 flex-column justify-content-center align-items-center">
        <h1 class="txt display-1"><strong>Aprenda Piano sem <span>{{ currentText }}</span></strong></h1>
        <h3 class="txt">A melhor plataforma para virar um verdadeiro pianista</h3>
      </div>
    </main>
  </template>
  
  <script>
  export default {
    data() {
      return {
        currentText: 'estresse!' 
      };
    },
    methods: {
      change() {
        const texts = ['estresse!', 'chatices!', 'problema!'];
        const randomIndex = Math.floor(Math.random() * texts.length);
        this.currentText = texts[randomIndex];
      }
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
  }
  .concerttransform:hover {
    transform: scale(1.0);
  }
  </style>
  