<template>
  <div class="sidebar">
    <div class="menu-item" @click="navigateTo('my-recordings')">
      <i class="icon video-icon"></i>
      <span class="menu-text">My Recordings</span>
    </div>
    <div class="menu-item" @click="navigateTo('requested')">
      <i class="icon share-icon"></i>
      <span class="menu-text">Requested</span>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    navigateTo(menu) {
      
      this.$router.push({ name: menu });
      
      
      console.log(`Navigate to ${menu}`);
    },
  },
};
</script>

<style scoped>
.sidebar {
  width: 306px;
  height: 100%; 
  background: #EBF2F6;
  padding-top: 20px; 
}

.menu-item {
  cursor: pointer;
  padding: 10px;
  margin-bottom: 10px;
  background-color: #d3d3d3;
  border-radius: 5px;
  display: flex;
  align-items: center;
}

.menu-text {
  font-size: 16px;
  font-weight: 300;
  margin-left: 10px;
  color: #21455E;
}

.icon {
  margin-right: 10px;
  width: 26px;
  height: 21px;
  opacity: 1;
}

.video-icon::before {
  content: url('@/assets/video-icon.png'); 
}

.share-icon::before {
  content: url('@/assets/share-icon.png'); 
}
</style>
