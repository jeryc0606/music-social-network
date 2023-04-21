<template>
    <div>
     <div class="py-4 mx-auto">
        <div class="flex flex-wrap font-bold text-gray-100">
            <div class="text-xl text-gray-900">Youtube Videos</div>
            <div class="w-full h-1 bg-green-500"></div>
            <div class="w-full mt-4">
                
                <RouterLinkButton 
                    btnText="Create Post"
                    color="green"
                    url="/account/create-post"
                    
                />
            </div>
          </div>
        </div>
        
        <div class="flex flex-wrap mb-4">
            <div class="w-full px-1 my-1 lg:w-1/2">
                
<div class="border-gray-200 rounded-lg ">
    <a href="#">
        <img class="rounded-t-lg" src="https://via.placeholder.com/500" alt="" />
    </a>
    <div class="p-2 md:p-4">
        <div class="text-lg ">
           <router-link to="" class="text-blue-500 underline hover:text-blue-600" >
            Test Title
           </router-link>
        </div>
        <p class="py-2">Location: test location</p>
        <p class="text-gray-darker text-md">Lorem ipsum dolor sit amet consectetur adipisicing elit. Assumenda nulla aliquam iste, dolore possimus impedit explicabo molestiae, vel cumque quaerat accusantium, quae odio modi accusamus optio ex libero suscipit soluta.
        </p>
        <div class="flex items-center justify-end mt-2">
            <router-link to="" class="px-2 py-1 text-sm font-bold text-white bg-blue-500 rounded-full hover:bg-blue-700" >
            Delete
           </router-link>
           <button to="" class="px-2 py-1 text-sm font-bold text-white bg-red-500 rounded-full hover:bg-red-700" >
            Edit-post
           </button>
        </div>
        
       
    </div>
</div>

            </div> 
        </div>
    </div>
</template>
<script setup>

 import RouterLinkButton from '../../../components/global/RouterLinkButton';

</script>