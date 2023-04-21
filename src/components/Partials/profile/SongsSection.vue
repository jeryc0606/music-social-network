<template>
    <div>
     <div class="py-4 mx-auto">
        <div class="flex flex-wrap font-bold text-gray-100">
            <div class="text-xl text-gray-900">Songs</div>
            <div class="w-full h-1 bg-green-500"></div>
            <div class="w-full mt-4">
                <RouterLinkButton 
                    class="ml-2"
                    btnText="Delete Song"
                    color="blue"
                    url="/account/delete-song"
                />
                <RouterLinkButton 
                    btnText="Add Song"
                    color="green"
                    url="/account/add-song"
                />
            </div>
        </div>
    </div>
        <div>
            <SongPlayer />
        </div>
     </div>
</template>
<script setup>
 import SongPlayer from './SongPlayer.vue'
 import RouterLinkButton from '../../../components/global/RouterLinkButton';

</script>