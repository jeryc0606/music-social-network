<template>
    <div id="Register">
        <div class="flex items-center justify-center w-full p-6">
          <div class="w-full max-w-xs">
            <div class="p-6 mb-6 bg-black rounded shadow">
              <h1 class="mb-6 text-lg font-thin text-gray-100">Lets get Rocking </h1>

              <div class="mb-4" >
                <TextInput
                 label="Firstname"
                 :labelColor="false"
                 placeholder="First Name"
                 v-model:input="firstName"
                 inputType="text"
                 error="this is test error"
                />
                </div>

                <div class="mb-4" >
                <TextInput
                 label="Last Name"
                 :labelColor="false"
                 placeholder="Last Name"
                 v-model:input="lastName"
                 inputType="text"
                 error="this is test error"
                />
                </div>


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

                <div class="mb-4" >
                <TextInput
                 label="Confirm Password"
                 :labelColor="false"
                 placeholder="Confirm Password"
                 v-model:input="confirmPassword"
                 inputType="text"
                 error="this is test error"
                />
                </div>



                
                  <button class="block w-full py-3 text-sm tracking-wide text-white bg-green-500 rounded-sm" type="submit"> Register </button>
            </div>
            <p class="text-center text-gray-900 text-md">
              Already have an Account?
              <router-link to="login" class="no-underline text-sky-400 hover:underline">
                  Login
              </router-link>
            </p>
          </div>
        </div>
    </div>
</template>

<script setup> 
import {ref} from 'vue';
import TextInput from '../components/global/TextInput.vue';

let firstName = ref(null)
let lastName = ref(null)
let email = ref(null)
let password = ref(null)
let  confirmPassword= ref(null)

</script>