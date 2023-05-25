<template>
  <div>
    <iframe
      width="100%"
      height="315"
      :src="`https://www.youtube.com/embed/2pZmKW9-I_k?list=PL4cUxeGkcC9gUgr39Q_yD6v-bSyMwKPUI`"
      title="video player"
      frameborder="0"
      allowfullscreen
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture; gyroscope;"
    >
    </iframe>
  </div>
</template>

<script lang="ts" setup>
const props = defineProps({
  videoId: {
    type: Number,
    required: true,
  },
});
</script>
<style scoped></style>
<!-- <iframe width="1024" height="576" src="https://www.youtube.com/embed/2pZmKW9-I_k?list=PL4cUxeGkcC9gUgr39Q_yD6v-bSyMwKPUI" title="TypeScript Tutorial #1 - Introduction &amp; Setup" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe> -->
