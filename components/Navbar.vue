<template>
  <nav>
    <div class="nav-banner">{{ banner }}</div>
    <div
      v-for="(value, index) in items"
      :key="index"
      class="nav-item">
      {{ value }}
    </div>
  </nav>
</template>
<script>
export default {
  props: {
    items: {
      default: function() {
        return ['บทความส์ สั้น!!', 'บทความส์ ยาว!!', 'วิดีโอส์']
      },
      type: Array
    },
    banner: {
      default: 'กระโปก JS',
      type: String
    }
  }
}
</script>
<style scoped>
.nav-banner {
  font-size: 25px;
  padding-left: 10px;
  padding-right: 10px;
}
.nav-item {
  font-size: 18px;
  padding-top: 10px;
  padding-bottom: 10px;
  padding-left: 20px;
  padding-right: 20px;
}
nav {
  display: flex;
  background-color: #f7c854;
  padding-top: 10px;
  padding-bottom: 10px;
}
</style>
