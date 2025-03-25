<template>
  <div class="teaser">
    <video class="teaser-video" autoplay loop muted>
      <source src="https://cdn.prod.website-files.com/601fd950d47be3916b6f3871/6223cf5edea9dbf1f479a9f0_pexels-rodnae-productions-7187405%20trimmed-transcode.mp4" type="video/mp4" />
    </video>
  </div>
</template>

<script>
export default {
  name: "Teaser",
};
</script>

<style scoped>
.teaser {
  width: 100%;
  height: 40rem; /* Limited height */
  overflow: hidden;
}

.teaser-video {
  width: 100%; /* Make the video fill the width */
  height: 100%; /* Make the video fill the height */
  object-fit: cover; /* Crop the video to fit the container */
  filter: grayscale(100%);
  }
</style>