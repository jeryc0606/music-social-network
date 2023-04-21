<template>
    <nav class="relative z-20 w-full px-4 bg-black text-white-200">
       <div class="container flex justify-between h-16 max-w-4xl mx-auto text-xs md:text-sm">
            <div class="flex items-center h-full"> 
                <router-link to="" class="flex items-center justify-center" >
                <div class="text-2xl text-white">
                <b>MSN</b>
                </div>
                </router-link>
            </div>
            <div class="flex items-center h-full">
                <FullScreenModal />
            </div>
       </div>
    </nav>
   </template>

<script setup>
 import FullScreenModal from '../../components/structure/FullScreenModal.vue';
</script>