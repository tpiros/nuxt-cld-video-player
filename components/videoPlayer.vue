<template>
  <video
    id="example-player"
    controls
    width="400"
    muted
    class="cld-video-player cld-video-player-skin-dark"
  ></video>
</template>
<script>
export default {
  mounted() {
    if (process.client) {
      const cld = cloudinary.Cloudinary.new({
        cloud_name: "tamas-demo",
        secure: true
      });
      const demoplayer = cld.videoPlayer("example-player");
      demoplayer.source("web-perf/IMG_0460", {
        transformation: { width: 400 }
      });
    }
  }
};
</script>
