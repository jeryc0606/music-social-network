<template>
    <div id="Register">
        <div class="flex items-center justify-center w-full p-6">
          <div class="w-full max-w-xs">
            <div class="p-6 mb-6 bg-black rounded shadow">
              <h1 class="mb-6 text-lg font-thin text-gray-100">Lets get Rocking Login </h1>

              <div class="mb-4" >
                <TextInput
                 label="Email"
                 :labelColor="false"
                 placeholder="Email"
                 v-model:input="email"
                 inputType="text"
                 error="this is test error"
                />
                </div>

                <div class="mb-4" >
                <TextInput
                 label="Password"
                 :labelColor="false"
                 placeholder="Password"
                 v-model:input="password"
                 inputType="text"
                 error="this is test error"
                />
                </div>
                <span class="text-red-500">
                    This is error Message
                  </span>
                  <button class="block w-full py-3 text-sm tracking-wide text-white bg-blue-500 rounded-sm" type="submit"> Login</button>
            </div>
            <p class="text-center text-gray-900 text-md">
              Don't have Account Yet?
              <router-link to="register" class="no-underline text-sky-400 hover:underline">
                  Register
              </router-link>
            </p>
          </div>
        </div>
    </div>
</template>

<script setup> 
import {ref} from 'vue';
import TextInput from '../components/global/TextInput.vue';

let email = ref(null)
let password = ref(null)

</script>