<template>
    <div>
        <button @click="open = !open" 
        class="px-2 py-1 font-semibold text-white bg-transparent rounded hover:bg-green-400 hover:text-white hover:border-transparent">
        <i class="fa-solid fa-bars fa-xl"></i>
        </button>
        <div v-show="open" class="fixed top-0 left-0 flex justify-center w-full h-full animated slideInDown faster backdrop-blur-sm">
            <div class="absolute w-full h-full bg-black opacity-75"></div>
            <div class="fixed pt-16 my-auto border-white w-80">
            <p class="text-2xl font-bold text-center text-white">Menu</p>
            
                <RouterLinkButton
                    class="w-full text-lg text-center text-gray-100" 
                    btnText="Profile"
                    color="green"
                    url="/account/profile" 
                />
                <RouterLinkButton
                    @click="open =!open"
                    class="w-full mt-4 text-lg text-center text-gray-100" 
                    btnText="Close"
                    color="red"  
                />
                
            
            </div>
        </div>
        
        
    </div>
   </template>

   <script setup>
        import {ref} from 'vue'
        import RouterLinkButton from '../global/RouterLinkButton.vue';
        let open = ref(false)
 </script>