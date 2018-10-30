<template>
  <div>
    <router-link :to="link">
      <img :src="image">
      <p>{{ title }}</p>
    </router-link>
  </div>
</template>
<script>
export default {
  props: {
    image: { default: 'https://via.placeholder.com/150', type: String },
    title: { default: 'กระโปก JS', type: String },
    link: { default: '/', type: String }
  }
}
</script>
<style scoped>
a {
  color: inherit;
  text-decoration: none;
}
div {
  width: 30%;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
  transition: 0.5s;
  padding: 20px;
}

img {
  width: 95%;
}
div:hover {
  box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
}
</style>
