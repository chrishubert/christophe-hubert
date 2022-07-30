<template>
  <div class="youtube-video-container">
    <iframe
      width="560"
      height="315"
      :src="'https://www.youtube.com/embed/' + ytCode"
      title="YouTube video player"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
      allowfullscreen
    ></iframe>
  </div>
</template>
<script>
export default {
  props: {
    ytCode: {
      type: String,
      default: 'dQw4w9WgXcQ'
    }
  }
}
</script>
<style scoped lang="scss">
.youtube-video-container {
  position: relative;
  overflow: hidden;
  width: 100%;
  margin-bottom: 2%;
}

.youtube-video-container::after {
  display: block;
  content: '';
  padding-top: 56.25%;
}

.youtube-video-container iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
</style>
