<template>
    <div id="centerCalltoAction">
        <div class="px-4 mx-auto text-center md:w-3/4 lg-:w-2/3">
            <h1 class="mb-3 text-4xl text-center text-gray-100 sm:text-5xl md:text-5xl leadin-tight">
                <b>Music Social Network</b>
                <p class="pt-2 text-xl text-center text-gray-300">
                    Login or Register now and join other like minded people all around the world who want to share there music
                </p>
                <p class="pt-2 text-xl text-center text-gray-300">
                    Let be the Music be your guide
                </p>
            </h1>
        </div>
        <div class="mt-6"></div>
        <div class="flex justify-between">
            <router-link class="w-full px-4 py-2 mr-1 text-2xl font-semibold text-center text-white bg-green-600 rounded-lg shadow-md cursor-pointer hover:bg-green-500 focus:outline-none focus:ring-2 focus:ring-green-400 focus:ring-opacity-75"  to="">Login</router-link>
        
            <router-link  class="w-full px-4 py-2 mr-1 text-2xl font-semibold text-center text-white bg-blue-600 rounded-lg shadow-md cursor-pointer hover:bg-blue-500 focus:outline-none focus:ring-2 focus:ring-blue-400 focus:ring-opacity-75" to="">Register</router-link>
        </div>
    </div>
    <div id="videoDarkOverlay"></div>
    <video id="Myvideo" autoplay muted loop>
        <source src="../../../../public/concert.mp4" type="video/mp4">
    </video>
</template>

<script setup></script>
<style lang="scss">
     #centerCalltoAction{
       width: 100%;
       position: absolute;
       left: 50%;
       top: 50%;
       -webkit-transform: translate(-50%, -50%);
       transform: translate(-50%, -50%);
     }
 #Myvideo{
    width: 100vw;
    height: 100vh;
    object-fit: cover;
    position:fixed;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    z-index: -2;
 }
 #videoDarkOverlay{
    width: 100vw;
    height: 100vh;
    object-fit: cover;
    position:fixed;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    z-index: -1;
    background-color: rgb(0,0,0,0.65);
 }
</style>