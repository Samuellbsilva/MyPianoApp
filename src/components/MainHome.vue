<template>

    <main class="d-flex h-100 w-100 flex-rown">
<div></div>
<div class="d-flex w-50 justify-content-center align-items-center">

<img class="w-100 concerttransform" src="../assets/MainPicture.png" alt="">

</div>
<div class="d-flex w-50 flex-column justify-content-center align-items-center">

<h1 class="txt display-1"><strong>Aprenda Piano sem <span class="">{{ change }}</span></strong></h1>
<h3 class="txt">A melhor plataforma para virar um verdadeiro pianista</h3>

</div>

    </main>
</template>



<script>

export default{

    computed: {
    change(){
        let j=0
       
           
        while (j<=300) {
        j++

        
        let mbraltr=Math.floor(Math.random() *2);

        switch (mbraltr) {
            case 0:
            
                return "estresse!"
               
                break;
        
                case 1:
                
                return "chatices!"
                
                break;
                case 2:
               
                return "problema!"
                
                break;
        
            default:
                break;
        }
    }
},
    }
    }
</script>


<style>

.txt{
    color: white;
}
.concerttransform:hover{
    transform:scale(1.0);
}
</style>
