<template>
  <div>
    <Navbar/>
    <Banner/>
    <ListCard
      title="วิดีโอล่าสุด"
      icon="https://svgshare.com/i/97h.svg"/>
    <ListCard
      title="บทความล่าสุด"
      icon="https://svgshare.com/i/97r.svg"/>
  </div>
</template>

<script>
import BlogCard from '@/components/Blog-card'
import Navbar from '@/components/Navbar'
import Banner from '@/components/banner'
import ListCard from '@/components/list-card'
export default {
  components: {
    BlogCard,
    Navbar,
    Banner,
    ListCard
  },
  head() {
    return {
      title: 'กระโปก JS',
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        {
          hid: 'description',
          name: 'description',
          content: 'กระโปก JS เป็นเว็บที่สอนเขียน JS แบบ ๐l๐'
        }
      ]
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Prompt:400,500');

html {
  font-family: 'Prompt', sans-serif;
}
button:focus,
input {
  outline: none;
}
</style>
