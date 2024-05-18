
<template>
    

<footer class="d-flex bg-dark  flex-wrap p-0 mt-5 " >
    <div class="d-flex w-25 align-items-center justify-content-center">
   
</div>
    <div class="d-flex flex-column w-50 align-items-center justify-content-center">
    <img src="../assets/icons8-electronic-music-64.png" class="rounded ml-5 " alt="">
    <p class="text-light"><strong>MyPiano</strong></p>
</div>

    <nav class=" d-flex w-25 justify-content-end space-between  flex-rown ">
    <div class="d-flex flex-column mr-4 ml-2 p-3 align-items-center" >
        <a href="http://" class="pr-2 pl-2">
            <img class="rounded-circle " src="../assets/SocialNetworks/icons8-github.gif" alt="GitHub">
        <p class="text-light"><strong>Github</strong></p>
        </a>
    </div>
    <div class="d-flex flex-column mr-2 ml-4 p-3 align-items-center" >
        <a href="http://" class="pr-2 pl-2">
            <img class="rounded-circle anim" src="../assets/SocialNetworks/icons8-instagram.svg" alt="GitHub">
        <p class="text-light"><strong>Instagram</strong></p>
        </a>
    </div>
  
  </nav>
</footer>

</template>

<script>

export default {        
}
    </script>

    <style>
*{
    text-decoration: none !important;
}
.anim{
    transition: transform 0.3s;

}
@keyframes pulse {
        0% {
            transform: scale(1.0);
        }
        50% {
            transform: scale(1.1);
        }
        100% {
            transform: scale(1.0);
        }
    }
    .anim{
        animation: pulse 2s infinite;
    }
img:hover{
    animation:none;
    transform: scale(1.1);
}
</style>