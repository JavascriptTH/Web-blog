<template>
  <div class="container">
    <h2 class="title"><img :src="icon">{{ title }}</h2>
    <div class="row">
      <BlogCard
        v-for="(value , index) in cardItems"
        :key="index"/>
    </div><button>More</button>
  </div>
</template>
<script>
import BlogCard from '@/components/Blog-card'
export default {
  components: {
    BlogCard
  },
  props: {
    title: {
      default: '',
      type: String
    },
    icon: {
      default: '',
      type: String
    },
    cardItems: {
      default: function() {
        return new Array(4)
      },
      type: Array
    },
    linkMore: {
      default: '',
      type: String
    }
  }
}
</script>
<style scoped>
.container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  margin-top: 10px;
}
.row {
  display: flex;
  flex-direction: row;
  justify-content: center;
  flex-wrap: wrap;
  width: 100%;
}
.title {
  border-bottom: 3px solid rgba(172, 172, 172, 0.4);
  padding-top: 10px;
  padding-bottom: 10px;
  width: 80%;
}

.title > img {
  width: 60px;
  margin-left: 20px;
  margin-right: 20px;
}
.more > button {
  float: right;
  background-color: #f7c854;
  border-color: #f7c854;
  border-radius: #f7c854;
  width: 80px;
  text-align: center;
  height: 30px;
  font-size: 16px;
  color: white;
  border-radius: 10px;
}

@media only screen and (max-width: 576px) {
  .more > button {
    margin: auto;
  }
}
</style>
