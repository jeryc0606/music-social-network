<template>
    <label for="" class="block text-xs font-bold tracking-wide text-gray-900 uppercase">
        {{ label }}
    </label>
   <textarea class="block w-full px-4 py-3 leading-tight text-gray-700 bg-white border border-gray-400 rounded appearance-none focus:outline-none focus:bg-white focus:border-gray-500"
   v-model="descriptionComputed" cols="30" rows="10" :placeholder="placeholder"></textarea>
   <span v-if="error" class="text-red-500">
        {{ error }}
   </span>
</template>

<script setup> 

import {defineProps, toRefs,computed, defineEmits} from 'vue'
const emit =defineEmits(['update:description']) 

const props = defineProps({
    label: String, 
    description: String,
    placeholder: {type:String, default:''},
    error: String
})
const {description, label, placeholder, error} = toRefs(props)

const descriptionComputed  = computed({
    get:() => description.value,
    set:(val) => emit('update:description', val)
})

</script>