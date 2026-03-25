<script setup lang="ts">
import { videos } from '@/videos.ts'

</script>

<template>
  <div style="width: 100%; text-align: center">
    <div v-for="video in videos" style="padding: 5px">
      <iframe width="560" height="315" :src="video.src" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
    </div>
  </div>
</template>
