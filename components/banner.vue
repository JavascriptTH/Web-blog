<template>
  <div class="banner">
    <img :src="image">
    <div class="center">{{ title }}</div>
  </div>
</template>
<script>
export default {
  props: {
    title: {
      default: 'กระโปก JS',
      type: String
    },
    image: {
      default: 'https://devahoy.com/assets/images/2014/12/javascript.png',
      type: String
    }
  }
}
</script>
<style scoped>
img {
  width: 100%;
  height: 250px;
  object-fit: cover;
  opacity: 0.5;
}

.center {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-size: 50px;
}
.banner {
  width: 100vw;
  position: relative;
  text-align: center;
}
</style>
