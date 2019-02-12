<template>
  <div class = "home">
    <VideoPlay :src = "src" :type = "type" />
  </div>
</template>

<script>/* eslint-disable */
  import VideoPlay from '@/components/VideoPlay.vue';

  export default {
    name: 'home',
    components: {
      // HelloWorld,
      // VideoPlay,
      VideoPlay
    },
    data() {
      return {
        src: 'rtmp://192.168.1.24:1935/live/leo',
        type: 'rtmp/flv'
      };
    }
  };
</script>
