<template>
    <div class="top-menu">
      <div class="logo">
        <img src="@/assets/logo-icon.png" alt="Logo Icon" class="logo-icon" />
        <span class="logo-text">Adilo</span>
      </div>
      <div class="menu-items">
        <div class="menu-item" @click="navigateTo('projects')">Projects</div>
        <div class="menu-item" @click="toggleAppsToolsDropdown">Apps & Tools</div>
        <div class="menu-item" @click="navigateTo('channels')">Channels</div>
        <div class="menu-item" @click="navigateTo('contacts')">Contacts</div>
        <div class="menu-item" @click="navigateTo('analytics')">Analytics</div>
        <div class="menu-item" @click="navigateTo('settings')">Settings</div>
  
        <div v-if="showAppsToolsDropdown" class="apps-tools-dropdown">
        
        </div>
      </div>
      <div class="user-info">
        <img src="@/assets/user-photo.png" alt="User Photo" class="user-photo" />
        <div class="user-details">
          <div class="user-name">Atuchukwu Chukwuemeka</div>
          <div class="user-email">user@example.com</div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        showAppsToolsDropdown: false,
      };
    },
    methods: {
      toggleAppsToolsDropdown() {
        this.showAppsToolsDropdown = !this.showAppsToolsDropdown;
      },
      navigateTo(menu) {
        
        console.log(`Navigate to ${menu}`);
      },
    },
  };
  </script>
  
  <style scoped>
  .top-menu {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 16px;
    background-color: #2c3e50;
    color: #ecf0f1;
  }
  
  .logo {
    display: flex;
    align-items: center;
  }
  
  .logo-icon {
    width: 40px;
    height: 40px;
    border-radius: 10px;
    background: #FBBD71;
    margin-right: 8px;
  }
  
  .logo-text {
    font-size: 28px;
    font-weight: bold;
    color: #21455E;
  }
  
  .menu-items {
    display: flex;
    align-items: center;
  }
  
  .menu-item {
    cursor: pointer;
    margin-right: 16px;
    font-size: 18px;
    font-weight: medium;
    color: #707070;
  }
  
  .user-info {
    display: flex;
    align-items: center;
  }
  
  .user-photo {
    width: 32px;
    height: 32px;
    border-radius: 50%;
    background-color: #3498db;
    margin-right: 8px;
  }
  
  .user-details {
    display: flex;
    flex-direction: column;
  }
  
  .user-name {
    font-size: 16px;
    font-weight: bold;
  }
  
  .user-email {
    font-size: 14px;
  }
  </style>
  