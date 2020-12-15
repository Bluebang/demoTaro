<template>
  <view class="index">
    <video
      id="myVideo"
      class="w100 h100"
      src="https://cloud.video.taobao.com//play/u/555657275/p/1/e/6/t/1/285650036342.mp4"
      :autoplay="false"
      :muted="false"
      controls="false"
      objectFit="fill"
      :initialTime="0"
      @timeupdate="onTimeUpdate"
      @ended="onEned"
      @play="onPlay"
    ></video>
  </view>
</template>

<script>
import './index.css';

export default {
  data() {
    return {
      msg: 'Hello world!',
    };
  },
  methods: {
    onPlay() {
      console.log('play');
    },
    onTimeUpdate(e) {
      let time = e.detail.currentTime;
      console.log(time);
    },
    onEned() {
      console.log('end');
    },
  },
};
</script>
