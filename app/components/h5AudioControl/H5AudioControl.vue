<template>
  <h5-audio-controls
    ref="h5AudioControlsRef"
    :src
  />
  <a
    href="javascript:"
    @click="trigger"
  >music trigger</a>
</template>

<script setup>
import { ref } from 'vue';
import H5AudioControls from '@cycjimmy/vue-h5-audio-controls';

const h5AudioControlsRef = ref(null);

const src = 'https://cycjimmy.github.io/staticFiles/media/Richard_Clayderman-LOVE_IS_BLUE.mp3';

const trigger = () => {
  if (h5AudioControlsRef.value.isPlaying()) {
    h5AudioControlsRef.value.pause();
  } else {
    h5AudioControlsRef.value.play();
  }
};
</script>
