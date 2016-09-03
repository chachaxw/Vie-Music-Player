<template lang="html">
  <div class="music-cover">
    <img :src="images" alt="" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      images: 'https://img3.doubanio.com/spic/s3737076.jpg',
    };
  },
};
</script>

<style scoped>

</style>
