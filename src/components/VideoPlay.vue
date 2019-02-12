<template>
  <div>
    <video id = "example_video_1" class = "video-js vjs-default-skin" controls preload = "auto" width = "800"
           height = "380"
           poster = "http://vjs.zencdn.net/v/oceans.png" data-setup = "{}">
      <source :src = src :type = type>
      <p class = "vjs-no-js">To view this video please enable JavaScript, and consider upgrading to a web browser that
        <a
          href = "http://videojs.com/html5-video-support/" target = "_blank">supports HTML5 video</a></p>
    </video>
  </div>
</template>

<script>
  import 'video.js/dist/video-js.min.css';
  import 'video.js/dist/video';

  export default {
    name: 'VideoPlay',
    props: ['src', 'type'],

  };
</script>

<style scoped>

</style>
