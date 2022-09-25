<template>
  <div ref="refAplayer">
    1
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted } from "vue";
import "aplayer/dist/APlayer.min.css";
import APlayer from "aplayer";
const refAplayer = ref(null);
onMounted(() => {
  const ap = new APlayer({
    container: refAplayer.value,
    // mini: false,
    autoplay: true,
    // theme: "#FADFA3",
    // loop: "all",
    // order: "random",
    // preload: "auto",
    // volume: 0.7,
    // mutex: true,
    // listFolded: false,
    // listMaxHeight: 90,
    // lrcType: 3,
    audio: [
      {
        name: "拜德盖Viigho",
        artist: "高雅先生",
        url: "拜德盖Viigho - 高雅先生.mp3",
        cover: "高雅先生.jpg",
      },
    ],
    fixed: true,
  });
  console.log("1", refAplayer);
});
</script>

<style>
</style>