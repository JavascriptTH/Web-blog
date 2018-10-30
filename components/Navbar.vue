<template>
  <nav>
    <div class="nav-banner">{{ banner }}</div>
    <div class="nav-items">
      <div
        v-for="(value, index) in items"
        :key="index"
        class="nav-item">
        {{ value }}
      </div>
    </div>
  </nav>
</template>
<script>
export default {
  props: {
    items: {
      default: function() {
        return ['บทความส์ สั้น!!', 'บทความส์ ยาว', 'วิดีโอส์']
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
}
.nav-items {
  display: inline-flex;
  justify-content: space-evenly;
  width: 30vw;
}
.nav-item {
  font-size: 18px;
}
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #f7c854;
  padding: 15px 20px;
}
</style>
