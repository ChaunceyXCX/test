<template>
    <div class="layout">
      <SideBar />
      <div class="content">
        <slot />
      </div>
    </div>
  </template>
  
  <script setup>
  </script>
  
  <style scoped>
  .layout {
    display: flex;
  }
  .content {
    flex-grow: 1;
    padding: 20px;
  }
  </style>
  