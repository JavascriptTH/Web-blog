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
.container {
  display: flex;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}
</style>
