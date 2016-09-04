<template>
  <div id="app">
    <div class="logo">
      <img src="assets/images/logo.svg" width="100%" height="100%">
    </div>
    <!-- <play-list></play-list> -->
    <player></player>
    <music-list></music-list>
  </div>
</template>

<script>
import store from './store/store';
// import PlayList from 'components/PlayList.vue';
import MusicList from 'components/MusicList.vue';
import Player from 'components/Player.vue';

export default {
  components: {
    MusicList, Player,
  },
  store,
};
</script>

<style>
  @import "assets/css/iconfont.css";

  html {
    height: 100%;
  }
  body {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100%;
    margin: 0;
    padding: 20px;
    box-sizing: border-box;
    background-color: rgba(255,222,144,1);
  }

  #app {
    color: #2c3e50;
    max-width: 800px;
    width: 100%;
    height: 560px;
    position: relative;
    border-radius: 4px;
    background-color: rgba(255,255,255,1);
    box-shadow: 5px 40px 70px -30px rgba(219, 149, 68, 0.8);
    font-family: Source Sans Pro, Helvetica, sans-serif;
    text-align: center;
  }

  .logo {
    width: 138px;
    padding: 10px 20px;
    margin: 0 auto;
  }
</style>
