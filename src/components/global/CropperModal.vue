<template>
    <label for="" class="block text-xs font-bold tracking-wide text-gray-900 uppercase">
        {{ label }}
    </label>
    <button
    class="inline-block px-4 py-3 mt-2 font-bold text-white no-underline bg-green-500 hover:bg-green-700" 
    @click="$emit('showModal',true)">
                    {{ btnText }}
    </button>
    
</template>

<script setup> 
import {defineProps, toRefs,} from 'vue'

const props = defineProps({btnText: String, label: String,})
const {btnText, label, } = toRefs(props)


</script>