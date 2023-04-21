<template>
    <button class="inline-block float-right px-4 py-3 mt-2 font-bold text-white no-underline bg-green-500 hover:bg-green-700" 
    @click="$emit('submit',true)">
                    {{ btnText }}
    </button>
    
</template>

<script setup> 
import {defineProps, toRefs,} from 'vue'

const props = defineProps({btnText: String,})
const {btnText} = toRefs(props)


</script>