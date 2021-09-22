<template>
  <md-card>
    <md-card-actions>
      <div class="md-subhead">
        <span>rtmp flash / 流媒体</span>
      </div>
      <md-button class="md-icon-button"
                 target="_blank"
                 href="https://github.com/surmon-china/vue-video-player/tree/master/examples/05-video.vue">
        <md-icon>code</md-icon>
      </md-button>
    </md-card-actions>
    <md-card-media>
      <div class="item">
        <div class="player">
          <video-player class="vjs-custom-skin" :options="playerOptions">
          </video-player>
        </div>
      </div>
    </md-card-media>
  </md-card>
</template>

<script>
  import 'videojs-flash'
  export default {
    data() {
      return {
        playerOptions: {
          height: '360',
          sources: [{
            type: "rtmp/mp4",
            src: "rtmp://58.200.131.2:1935/livetv/cctv1"
          }],
          techOrder: ['flash'],
          autoplay: false,
          controls: true,
          poster: "https://surmon-china.github.io/vue-quill-editor/static/images/surmon-9.jpg"
        }
      }
    }
  }
</script>

