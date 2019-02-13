<template>
  <div class="home">
    <ul>
      <li v-for="(video,index) in videos" :key="index">
        <VideoPlay :src="video.src" :type="video.type"/>
      </li>
    </ul>
  </div>
</template>

<script>
/* eslint-disable */
import VideoPlay from "@/components/VideoPlay.vue";

export default {
  name: "home",
  components: {
    VideoPlay
  },
  data() {
    return {
      videos: [
        {
          src: "rtmp://192.168.0.211:1935/live/leo",
          type: "rtmp/flv"
        }
      ]
    };
  }
};
</script>
