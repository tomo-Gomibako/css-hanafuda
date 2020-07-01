<template>
  <card-frame>
    <div class="container">
      <div class="tsuki" />
      <div class="yama" />
    </div>
  </card-frame>
</template>

<script>
import CardFrame from '@/components/CardFrame'
export default {
  components: {
    'card-frame': CardFrame
  }
}
</script>

<style scoped>
  .container {
    width: 100%;
    height: 100%;
    background-color: orangered;
  }

  .tsuki {
    position: relative;
    top: 13%;
    left: 7%;
    width: 70%;
    height: 44%;
    border-radius: 50%;
    background-color: white;
  }

  .yama {
    position: relative;
    bottom: -14%;
    width: 100%;
    height: 42%;
    clip-path: ellipse(100% 135% at 37% 135%);
    background-color: black;
  }
</style>
