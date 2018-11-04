<template>
  <div>
    <nav>
      <div class="nav-banner">{{ banner }}</div>
      <!-- normal navbar -->
      <div class="nav-items">
        <div
          v-for="(value, index) in items"
          :key="index"
          class="nav-item">
          {{ value }}
        </div>
      </div>
      <!-- menu button -->
      <span 
        class="menu-button"
        @click="showMenu" >
        <fa
          :icon="faBars"
          size="2x" />
      </span>
    </nav>
    <!-- mobile navbar -->
    <div
      v-show="isShowed"
      class="mobile-nav-items">
      <div
        v-for="(value, index) in items"
        :key="index"
        class="mobile-nav-item">
        {{ value }}
      </div>
    </div>
  </div>
</template>
<script>
// https://www.npmjs.com/package/vue-fa
import Fa from 'vue-fa'
import { faBars } from '@fortawesome/free-solid-svg-icons'

export default {
  components: {
    Fa
  },
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
  },
  data() {
    return {
      faBars,
      isShowed: false
    }
  },
  methods: {
    showMenu: function(event) {
      this.isShowed = !this.isShowed
    }
  }
}
</script>
<style scoped>
.nav-banner {
  font-size: 25px;
  font-weight: 500;
}
.nav-items {
  font-size: 18px;
  font-weight: 500;
  display: inline-flex;
}
.nav-item {
  margin: 0 15px;
}
nav {
  width: 100vw;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #f7c854;
  padding: 15px 20px;
  box-shadow: 0px 1px rgba(0, 0, 0, 0.3);
}
.mobile-nav-items {
  display: none;
}
.menu-button {
  display: none;
}
@media screen and (max-width: 575.98px) {
  .menu-button {
    display: block;
  }
  .mobile-nav-items {
    display: flex;
    flex-flow: column nowrap;
    align-items: center;
    background: #f7c854;
  }
  .mobile-nav-item {
    font-size: 20px;
    margin: 10px;
  }
  .nav-items {
    display: none;
  }
}
</style>
