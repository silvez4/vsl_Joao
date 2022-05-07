<template>
  <div>
    <div class="custom-shape-divider-top-1651906812">
      <svg
        data-name="Layer 1"
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 1200 120"
        preserveAspectRatio="none"
      >
        <path
          d="M985.66,92.83C906.67,72,823.78,31,743.84,14.19c-82.26-17.34-168.06-16.33-250.45.39-57.84,11.73-114,31.07-172,41.86A600.21,600.21,0,0,1,0,27.35V120H1200V95.8C1132.19,118.92,1055.71,111.31,985.66,92.83Z"
          class="shape-fill"
        ></path>
      </svg>
    </div>
    <div class="bg-black px-4 py-6">
      <div class="mx-auto videoP max-w-2xl">
        <video-player
          SameSite="None"
          src="https://www.youtube.com/watch?v=ZDUS1qrAtKY"
        />
      </div>
    </div>
  </div>
</template>

<script>
import VideoPlayer from "nuxt-video-player";
require("nuxt-video-player/src/assets/css/main.css");

export default {
  name: "Video",
  components: {
    VideoPlayer,
  },
};
</script>
