<template>
  <div class="frame-container">
    <slot />
    <div class="frame" />
  </div>
</template>

<style scoped>
  .frame-container {
    width: 340px;
    height: 540px;
    /* border: 7px solid #444; */
    clip-path: polygon(0% 0%, 100% 0%, 100% 100%, 0% 100%);
  }

  .frame {
    position: relative;
    top: -100%;
    width: 100%;
    height: 100%;
    border: 7px solid #444;
  }
</style>
