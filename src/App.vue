<template>
  <div id="app">
    <div class="logo">
      <img src="assets/images/logo.svg" width="100%" height="100%">
    </div>
    <play-list></play-list>
  </div>
</template>

<script>
import store from './store/store';
import PlayList from 'components/PlayList.vue';

export default {
  components: {
    PlayList,
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
    background-color: rgba(255,222,144,1);
  }

  #app {
    color: #2c3e50;
    max-width: 800px;
    width: 100%;
    height: 500px;
    position: relative;
    border-radius: 4px;
    background-color: rgba(255,255,255,1);
    box-shadow: 5px 40px 80px -30px rgba(219, 149, 68, 0.6);
    font-family: Source Sans Pro, Helvetica, sans-serif;
    text-align: center;
  }

  .logo {
    width: 138px;
    padding: 10px 20px;
    margin: 0 auto;
  }
</style>
