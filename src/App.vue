<script setup lang="ts">
const title = import.meta.env.VITE_APP_TITLE;
</script>

<template>
  <div class="pageView keyboard_foot">
    <div class="content">
      <div>环境：{{ title }}</div>
    </div>
    <div class="tab-bar safe-bottom">
      <div class="inner">h5底部安全高度</div>
    </div>
  </div>
</template>

<style scoped>
.pageView {
  display: flex;
  flex-direction: column;
  overflow: hidden;
  height: 100vh;
  padding-top: constant(safe-area-inset-top); /* iOS */
  padding-top: env(safe-area-inset-top); /* Android */
  padding-bottom: constant(safe-area-inset-bottom); /* iOS */
  padding-bottom: env(safe-area-inset-bottom); /* Android */
  box-sizing: border-box;
}
.content {
  flex: 1;
  background-color: yellowgreen;
}
.tab-bar {
  height: 50px;
  background-color: springgreen;
}
.inner {
  height: 100%;
  background-color: lightblue;
}
</style>
