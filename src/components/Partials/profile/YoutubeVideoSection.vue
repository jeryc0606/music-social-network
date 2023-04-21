<template>
    <div>
     <div class="py-4 mx-auto">
        <div class="flex flex-wrap font-bold text-gray-100">
            <div class="text-xl text-gray-900">Youtube Videos</div>
            <div class="w-full h-1 bg-green-500"></div>
            <div class="w-full mt-4">
                <RouterLinkButton 
                    class="ml-2 hover:bg-red-500"
                    btnText="Delete Youtube Videos"
                    color="blue"
                    url="/account/delete-youtube-video"
                    
                />
                <RouterLinkButton 
                    btnText="Add Youtube Videos"
                    color="green"
                    url="/account/add-youtube-video"
                    
                />
            </div>
          </div>
        </div>
        
        <div class="flex flex-wrap mb-4">
            <div class="w-full px-1 my-1 lg:w-1/2">
                <div class="text-xl text-gray-900">Video Title</div>
                <iframe src="https://www.youtube.com/embed/GZE2umwHqL8?autoplay=0" class="w-full h-60" ></iframe>
            </div> 
        </div>
    </div>
</template>
<script setup>

 import RouterLinkButton from '../../../components/global/RouterLinkButton';

</script>