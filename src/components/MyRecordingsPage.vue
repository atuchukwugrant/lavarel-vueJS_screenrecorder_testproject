<template>
    <div class="my-recordings-page" v-if="showPage">
      <div class="top-buttons">
        <div class="button" @click="handleButtonClick('Sort by Date')">
          <i class="icon sort-icon"></i>
          <span>Sort by Date</span>
        </div>
        <div class="button" @click="handleButtonClick('Add Filter')">
          <i class="icon filter-icon"></i>
          <span>Add Filter</span>
        </div>
        <div class="button" @click="handleButtonClick('New Request')">
          <i class="icon request-icon"></i>
          <span>New Request</span>
        </div>
        <div class="button" @click="handleButtonClick('Start Recording')">
          <i class="icon record-icon"></i>
          <span>Start Recording</span>
        </div>
      </div>

      <div class="center-content">
        <h2>Say hello to the world!</h2>
        <p>Record your first video/audio and share it with your team, friends, followers, and customers.</p>
        <div class="center-buttons">
          <div class="button" @click="handleButtonClick('Start Recording')">
            <i class="icon record-icon"></i>
            <span>Start Recording</span>
          </div>
          <div class="button" @click="handleButtonClick('New Request')">
            <i class="icon request-icon"></i>
            <span>New Request</span>
          </div>
        </div>
      </div>

      <div class="bottom-content">
        <img src="@/assets/bottom-image.jpg" alt="Bottom Image" class="bottom-image" />
        <div class="bottom-text">
          <p>Want more controls & better quality recording?</p>
          <button @click="handleButtonClick('Download Desktop Recorder')">Download the desktop recorder</button>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        showPage: false,
      };
    },
    methods: {
      handleButtonClick(action) {

        console.log(`Button clicked: ${action}`);
      },
    },
  };
  </script>
  
  <style scoped>
  .my-recordings-page {
    opacity: 0;
    transition: opacity 0.5s ease-in-out;
  }
  
  .my-recordings-page.show {
    opacity: 1;
  }
  
  
  
  .button {
    cursor: pointer;
    display: flex;
    align-items: center;
    margin-right: 20px;
    padding: 10px;
    border: 1px solid #3498db;
    border-radius: 5px;
    transition: background-color 0.3s ease-in-out, color 0.3s ease-in-out;
  }
  
  .button:hover {
    background-color: #3498db;
    color: #fff;
  }
  
  .icon {
    margin-right: 8px;
    
  }
  
  .center-content {
    margin-top: 20px;
    text-align: center;
  }
  
  .center-buttons {
    margin-top: 20px;
  }
  
  .bottom-image {
    width: 100%;
  }
  
  .bottom-text {
    margin-top: 20px;
  }
  
  </style>
  