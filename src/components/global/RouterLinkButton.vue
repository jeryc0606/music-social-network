<template>
    <router-link  :class="[color ? 'hover:bg-'+ color + '-500 border-' + color + '-500' : '']" class="float-right px-4 py-2 font-semibold text-gray-900 bg-transparent border rounded hover:text-white hover:border-transparent " :to="url">
                    {{ btnText }}
    </router-link>
    
</template>

<script setup> 
import {defineProps, toRefs,} from 'vue'

const props = defineProps({btnText: String, url:{type:String, default:''}, color:String})
const {btnText, url, color} = toRefs(props)


</script>