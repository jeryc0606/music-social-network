
<template>
    <div id="EditProfile" class="container max-w-4xl px-6 pt-20 pb-20 mx-auto ">
        <div class="text-xl text-gray-900">Edit Profile</div>
            <div class="w-full h-1 bg-green-500"></div>
            <Cropper-Modal/>
            <div class="flex flex-wrap mt-4 mb-6">
                <div class="w-full px-3 md:w-1/2">
                <TextInput
                    label="First Name"
                    placeholder="John"
                    v-model:input="firstName"
                    inputType="text"
                    error="this is test error"
                />
                </div>
                <div class="w-full px-3 md:w-1/2">
                <TextInput
                    label="Lastname"
                    placeholder="doe"
                    v-model:input="lastName"
                    inputType="text"
                    error="this is test error"
                />
                </div>
            </div>
            <div class="flex flex-wrap mt-4 mb-6">
                <div class="w-full px-3 md:w-1/2">
                <TextInput
                    label="Location"
                    placeholder="Olongapo"
                    v-model:input="location"
                    inputType="text"
                    error="this is test error"
                />
                </div>
            </div>
            <div class="flex flex-wrap mt-4 mb-6">
                <div class="w-full px-3 md:w-1/2">
                <DisplayCropperButton
                  label="Profile Image"
                  btnText="Update Profile Image"
                />
                </div>
            </div>
            <div class="flex flex-wrap mt-4 mb-6">
                <div class="w-full px-3 ">
             <TextArea
                  label="Description"
                  placeholder="Please Enter some information"
                  v-model="description"
                  error="This is error"
             />

                </div>
            </div>
            <div class="flex flex-wrap mt-8 mb-6">
                <div class="w-full px-3 ">
                    <SubmitFormButton
                    btnText="Update Profile"/>
                </div>
            </div>
    </div>
    
</template>
<script setup>
import {ref} from 'vue'
import TextInput from '@/components/global/TextInput.vue';
import CropperModal from '@/components/global/CropperModal.vue';
import DisplayCropperButton from '@/components/global/DisplayCropperButton.vue';
import TextArea from '@/components/global/TextArea.vue';
import SubmitFormButton from '@/components/global/SubmitFormButton.vue';

let firstName =ref(null)
let lastName =ref(null)
let location=ref(null)
</script>
