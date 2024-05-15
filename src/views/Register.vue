<template>

<div>

<FormLogReg />
</div>
  
  </template>
  
  <style>

  @keyframes gradient {
    0%{background-position:0% 50%}
    50%{background-position:100% 50%}
    100%{background-position:0% 50%}
}
  body{
    background: linear-gradient(90deg, rgba(2,0,36,1) 0%, rgb(6, 6, 161) 35%, rgb(0, 0, 0) 100%);
  background-size: 400% 400%;
  animation: gradient 8s linear infinite;
  }
  </style>
  <script>
import  FormLogReg from'@/components/FormLogReg.vue'  ;
export default {

  components:{
    FormLogReg
  }
}
</script>