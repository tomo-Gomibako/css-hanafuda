<template>
  <card-frame>
    <div class="container">
      <div class="sakura-1">
        <sakura class="border" />
        <sakura class-name="light" />
      </div>
      <div class="sakura-2">
        <sakura class="border" />
        <sakura class-name="dark" />
      </div>
    </div>
  </card-frame>
</template>

<script>
import CardFrame from '@/components/CardFrame'
import Sakura from '@/components/parts/Sakura'
export default {
  components: {
    'card-frame': CardFrame,
    Sakura
  }
}
</script>

<style scoped>
  .container {
    width: 100%;
    height: 100%;
    background-color: white;
  }

  .sakura-1 {
    position: relative;
    width: 54%;
    height: 34%;
  }
  .sakura-2 {
    position: relative;
    width: 54%;
    height: 34%;
  }
</style>
