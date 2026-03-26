<script setup lang="ts">
import { videos } from '@/videos.ts'

const width = (window.innerWidth > 0) ? window.innerWidth : screen.width;
const videoWidth = width > 570 ? 560 : width - 10
const videoHeight = Math.floor(videoWidth / 1.77777778)

</script>

<template>
  <div style="width: 100%; text-align: center">
    <p style="color: white; font-family: Roboto, Helvetica, Arial, sans-serif">Weitere Infos findest du hier: <a style="color: white" href="https://sgbaselfricktal.ch/fliegen-lernen/">Fliegen lernen</a></p>
    <div v-for="video in videos" style="padding: 5px">
      <iframe style="max-width: calc(100% - 10px)" :width="videoWidth" :height="videoHeight" :src="video.src" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
    </div>
  </div>
</template>
