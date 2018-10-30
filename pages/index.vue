<template>
  <div>
    <Navbar/>
    <Banner/>
    <BlogCard/>
  </div>
</template>

<script>
import BlogCard from '@/components/Blog-card'
import Navbar from '@/components/Navbar'
import Banner from '@/components/banner'
export default {
  components: {
    BlogCard,
    Navbar,
    Banner
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Prompt:400,500');

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
