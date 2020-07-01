<template>
  <card-frame>
    <div class="container">
      <div class="tsuki" />
      <matsu class="matsu-1" />
      <matsu class="matsu-2" />
    </div>
  </card-frame>
</template>

<script>
import CardFrame from '@/components/CardFrame'
import Matsu from '@/components/parts/Matsu'
export default {
  components: {
    'card-frame': CardFrame,
    Matsu
  }
}
</script>

<style scoped>
  .container {
    width: 100%;
    height: 100%;
    background-color: white;
  }

  .tsuki {
    position: relative;
    top: -22%;
    right: -33%;
    width: 82%;
    height: 52%;
    border-radius: 50%;
    clip-path: rect(10px, 10px, 10px, 10px);
    background-color: orangered;
  }

  .matsu-1 {
    position: relative;
    top: -50%;
    transform: translate(44%, 0);
  }
  .matsu-2 {
    position: relative;
    top: -150%;
    transform: translate(-64%, 0);
  }
</style>
