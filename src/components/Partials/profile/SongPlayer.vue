<template>
       <div class="bg-green-500 rounded">
           <div id="aplayer"></div>
       </div>
</template>
<script setup>
    import { onMounted } from 'vue';
    import APlayer from 'aplayer'
    import 'aplayer/dist/APlayer.min.css';
    onMounted(()=>{
        thePlayer()
    })
    
    const thePlayer = () =>{
    new APlayer({
    container: document.getElementById('aplayer'),
    audio: [
        {
        name: 'First Song',
        artist: 'artist',
        url: '/music/cinematic-time-lapse-115672.mp3',
        cover: 'cover.jpg'
        },
        {
        name: 'Second Song',
        artist: 'artist',
        url: '/music/inspiring-emotional-uplifting-piano-112623.mp3',
        cover: 'cover.jpg'
        }
     ]
   });
    }
</script>