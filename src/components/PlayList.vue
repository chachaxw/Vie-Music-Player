<template>
  <div class="play-list-btn">
    <i class="iconfont icon-menu"></i>
  </div>
  <div class="music-play-list">
    <h4>Play List</h4>
    <ul>
      <li class="flex-box" v-for="el in playList">
        <div class="flex-item" v-text="el.songName"></div>
        <div class="music-owner" v-text="el.singer">五月天</div>
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
  .play-list-btn {
    position: absolute;
    right: 20px;
  }
  .iconfont {
    font-size: 22px;
  }
  .music-play-list {
    width: 60%;
    height: 414px;
    position: absolute;
    margin-top: 30px;
    right: 0;
  }
  .music-play-list h4 {
    background-color: #f5f5f5;
    padding: 10px;
    margin: 0;
    color: #444;
  }
  .music-play-list ul {
    list-style: none;
    margin: 0;
    padding: 0;
  }
  .music-play-list li:nth-child(2n) {
    background-color: #f5f5f5;
  }
  .flex-box {
    display: flex;
    padding: 8px 16px;
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
  .music-owner {
    width: 160px;
  }
  .music-duration {
    text-align: right;
    width: 60px;
  }
</style>
