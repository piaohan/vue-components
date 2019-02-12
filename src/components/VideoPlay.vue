<template>
  <div>
    <video id = "my-video" class = "video-js vjs-default-skin" controls preload = "auto" width = "800"
           height = "380"
           poster = "http://vjs.zencdn.net/v/oceans.png" data-setup = "{}"
    >
      <source :src = src :type = type>
      <p class = "vjs-no-js">To view this video please enable JavaScript, and consider upgrading to a web browser that
        <a
          href = "http://videojs.com/html5-video-support/" target = "_blank">supports HTML5 video</a></p>
    </video>
  </div>
</template>

<script>/* eslint-disable */
import 'video.js/dist/video-js.min.css';
import 'video.js/dist/video';
import videojs from 'video.js';

export default {
  name: 'VideoPlay',
  props: ['src', 'type'],
  mounted() {
    videojs('my-video', {
      autoplay: true,
      poster: "https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1550011029545&di=033fc8c11c89d3f79cd2ef0035fef460&imgtype=0&src=http%3A%2F%2Fpic.58pic.com%2F58pic%2F15%2F57%2F62%2F81U58PICpWs_1024.jpg",
    }, function () {
      this.play();
    });
  }
};
</script>

<style scoped>

</style>
