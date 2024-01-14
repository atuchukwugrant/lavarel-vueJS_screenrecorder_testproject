

<template>
    <div class="logo">
      <img src="@/assets/logo-icon.png" alt="Logo Icon" class="logo-icon" />
      <span class="logo-text">Adilo</span>
    </div>
  </template>
  
  <script>
  export default {
    
  };
  </script>
  
  <style scoped>
  .logo {
    display: flex;
    align-items: center;
  }
  
  .logo-icon {
    
    top: 22px;
    left: 51px;
    width: 40px;
    height: 40px;
    
    background: #FBBD71 0% 0% no-repeat padding-box;
    border-radius: 10px;
    opacity: 1;
  }
  
  .logo-text {
    
    top: 27px;
    left: 109px;
    width: 70px;
    height: 31px;
    
    text-align: left;
    font: normal normal bold 28px/32px Helvetica;
    letter-spacing: 0px;
    color: #21455E;
    opacity: 1;
  }
  </style>
  