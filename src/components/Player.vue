<template lang="html">
  <div class="music-player">
    <div class="music-cover">
      <img :src="images" alt="" />
    </div>
    <div class="song-name" v-text="tracks"></div>
    <div class="album-info">专辑：{{album}}</div>
    <div class="author">演唱者：{{author}}</div>
    <div class="track-bar">
      <span class="start-time" v-text="start"></span>
      <div class="progress-line">
        <div class="progress" :style="{'width': '40%'}"></div>
      </div>
      <span class="end-time" v-text="end"></span>
    </div>
    <div class="player-controllers">
      <span class="prev-btn"><i class="iconfont icon-prev"></i></span>
      <span class="play-btn"><i class="iconfont icon-play"></i></span>
      <span class="next-btn"><i class="iconfont icon-next"></i></span>
      <span class="model-btn"><i class="iconfont icon-loop"></i></span>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      images: 'https://img3.doubanio.com/spic/s1425762.jpg',
      author: '周杰伦',
      album: '十一月的萧邦',
      tracks: '夜曲',
      start: '01:30',
      end: '03:46',
    };
  },
};
</script>

<style scoped>
  .music-player {
    font-size: 12px;
    text-align: center;
  }
  .music-cover {
    width: 60px;
    height: 60px;
    margin: 0 auto;
    border-radius: 4px;
    overflow: hidden;
  }
  .music-cover img {
    width: 100%;
    height: 100%;
  }
  .author {
    color: rgb(83,88,97);
  }
  .song-name,
  .album,
  .author {
    padding: 8px;
  }
  .track-bar {
    display: flex;
    width: 500px;
    margin: 10px auto;
    justify-content: center;
    align-items: center;
  }
  .track-bar .start-time,
  .track-bar .end-time {
    width: 60px;
    display: inline-block;
  }
  .track-bar .progress-line {
    flex: 1 auto;
    height: 4px;
    border-radius: 2px;
    background-color: rgb(234,235,236);
  }
  .track-bar .progress {
    background-color: rgb(83,88,97);
    height: 100%;
    border-radius: 2px;
  }
  .player-controllers {
    margin-top: 20px;
    display: flex;
    position: relative;
    align-items: center;
    justify-content: center;
  }
  .play-btn {
    display: inline-block;
    width: 56px;
    height: 56px;
    border-radius: 50%;
    line-height: 54px;
    margin: auto 15px;
    background-color: rgb(224,124,82);
    box-shadow: 0 0 4px rgba(216,95,53,.5);
  }
  .play-btn i {
    color: #fff;
    font-size: 28px;
  }
  .prev-btn,
  .next-btn {
    display: inline-block;
    width: 32px;
    height: 32px;
    line-height: 32px;
    border-radius: 50%;
    background-color: #fff;
    box-shadow: 0 0 6px rgba(83,87,97,.15);
  }
  .prev-btn i,
  .next-btn i {
    font-size: 12px;
  }
  .model-btn {
    position: absolute;
    top: 50%;
    margin-left: 40px;
    margin-top: -12px;
  }
  .model-btn i{
    font-size: 20px;
    color: rgb(224,124,82);
  }
</style>
