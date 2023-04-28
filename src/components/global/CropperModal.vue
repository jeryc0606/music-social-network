<template>
   <div class="relative z-10">
        <div class="fixed inset-0 transition-opacity bg-opacity-75 bg-gray-50"></div>
            <div class="fixed inset-0 z-10 mt-6 overflow-y-auto">
                
             <div class="flex items-center justify-center min-h-full p-4 py-2">

                <div class="relative mt-10 overflow-hidden text-left transition-all transform bg-white rounded-lg shadow-xl mx-w-4xl">
                        
                    <div class="p-6 px-4 pt-5 pb-4 bg-white">
                        <div class="flex-items-center">
                            <div class="mt-3 text-left">
                                    <h3 class="text-xl font-medium leading-6 text-gray-900">Crop Image</h3>
                                    <div class="flex flex-wrap my-4">
                                        <label class="block mb-2 text-xs font-bold tracking-wide text-gray-700 uppercase">
                                            Select Image
                                        </label>
                                        <div class="w-full mb-3">
                                            <input type="file" class="block w-full px-3 py-1.5 form-control text-base font-normal text-gray-700 bg-white bg-clip bg-clip-padding border border-solid border-gray-400 rounded transition ease-in-out m-0 focus:text-gray-700 focus:bg-white focus:border-blue-600 focus-outline-none" id="image" ref="fileInput" @change=" getUploadedImage">
                                        </div>
                                    </div>
                                    <div class="flex justify-center max-w-2xl">
                                        <Cropper
                                        ref="cropper"
                                        :src= "uploadedImage"
                                        :stencil-props="{
                                          aspectRatio: 10/12
                                        }"
                                        @change="change"
                                      />
                                    </div>
                                    <div class="flex flex-row-reverse px-4 pb-3">
                                        <button type="button" class="inline-flex justify-center w-auto px-4 py-2 ml-3 text-sm font-medium text-white bg-blue-600 border border-transparent rounded-md shadow-sm hover:bg-blue-700 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:ring-offset-2">
                                            Crop Image
                                        </button>
                                        <button type="button" class="inline-flex justify-center w-auto px-4 py-2 ml-3 text-sm font-medium text-white bg-red-600 border border-transparent rounded-md shadow-sm hover:bg-red-700 focus:outline-none focus:ring-2 focus:ring-red-500 focus:ring-offset-2">
                                            Cancel
                                        </button>
                                    </div>
                            </div>
                        </div>
                    </div>
                </div>  
        </div> 
    </div>     
</div>
</template>

<script setup> 
import {ref} from 'vue'
import { Cropper } from 'vue-advanced-cropper'
import 'vue-advanced-cropper/dist/style.css';
 
let fileInput =ref(null)
let cropper =ref(null)
let uploadedImage=ref(null)

const getUploadedImage = (e) =>{
    const file = e.target.files[0]
    uploadedImage.value = URL.createObjectURL(file)
    console.log(uploadedImage.value)
}

</script>