<template>
  <div class="music-play-list">
    <ul>
      <li class="flex-box" v-for="el in playList">
        <div class="flex-item">
          <i class="iconfont icon-circle"></i>
          <span>{{el.songName}}</span></div>
        <div class="music-owner">歌手-{{el.singer}}</div>
        <div class="music-duration" v-text="el.duration"></div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      playList: [
        {
          songName: 'OAOA',
          singer: '五月天',
          duration: '05:20',
        },
        {
          songName: 'Four Seasons',
          singer: '滨崎步',
          duration: '04:20',
        },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .music-play-list {
    margin-top: 30px;
  }
  .music-play-list ul {
    list-style: none;
    margin: 0;
    padding: 0;
  }
  .music-play-list li{
    border-top: 1px #ececec solid;
  }
  .music-play-list li:last-child {
    border-bottom: 1px #ececec solid;
  }
  .flex-box {
    display: flex;
    padding: 28px 30px 28px 40px;
    width: 100%;
    color: #444;
    font-size: 13px;
    line-height: 1;
    text-align: left;
    justify-content: center;
    align-items: center;
    box-sizing: border-box;
  }
  .flex-item {
    flex: 1 auto;
  }
  .flex-item .iconfont {
    font-size: 20px;
    margin-right: 15px;
    display: inline-block;
    vertical-align: middle;
  }
  .music-owner {
    width: 280px;
  }
  .music-duration {
    text-align: right;
    width: 60px;
  }
</style>
