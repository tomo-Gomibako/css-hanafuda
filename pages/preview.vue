<template>
  <div class="preview-container">
    <jan-c />
    <mar-c />
    <aug-c />
  </div>
</template>

<script>
import JanC from '@/components/1-court'
import MarC from '@/components/3-court'
import AugC from '@/components/8-court'
export default {
  components: {
    JanC,
    MarC,
    AugC
  }
}
</script>

<style>
  .preview-container {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-gap: 10px;
    grid-auto-rows: minmax(100px, auto);
  }
</style>
