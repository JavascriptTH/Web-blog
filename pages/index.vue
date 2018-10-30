<template>
  <div>
    <Navbar/>
    <BlogCard/>
  </div>
</template>

<script>
import BlogCard from '@/components/Blog-card'
import Navbar from '@/components/Navbar'
export default {
  components: {
    BlogCard,
    Navbar
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Prompt');

html {
  font-family: 'Prompt', sans-serif;
}

.container {
  display: flex;
}

.title {
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}
</style>
