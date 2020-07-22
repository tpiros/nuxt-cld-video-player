<template>
  <client-only>
    <div>
      <video-player />
    </div>
  </client-only>
</template>

<script>
export default {
  head() {
    return {
      script: [
        {
          vmid: 'extscript',
          src:
            "https://unpkg.com/cloudinary-core@2.10.3/cloudinary-core-shrinkwrap.min.js",
          defer: true,
        },
        {
          vmid: 'extscript',
          src:
            "https://unpkg.com/cloudinary-video-player@1.4.1/dist/cld-video-player.min.js",
          defer: true,
        }
      ]
    };
  }
};
</script>
