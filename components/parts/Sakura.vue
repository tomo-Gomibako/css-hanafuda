<template>
  <div class="sakura">
    <div class="petal top">
      <div :class="className" />
    </div>
    <div class="petal up-right">
      <div :class="className" />
    </div>
    <div class="petal down-right">
      <div :class="className" />
    </div>
    <div class="petal down-left">
      <div :class="className" />
    </div>
    <div class="petal up-left">
      <div :class="className" />
    </div>
    <div class="sepal">
      <div>
        <div />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    className: {
      type: String,
      default: 'light'
    }
  }
}
</script>

<style scoped>
  .sakura {
    position: absolute;
    width: 100%;
    height: 100%;
  }

  .petal {
    position: absolute;
    top: 15%;
    left: 30%;
    width: 33%;
    height: 66%;
    clip-path: ellipse(35% 50% at 50% 50%);
  }
  .petal > div {
    width: 100%;
    height: 100%;
    clip-path: polygon(0% 0%, 30% 0%, 50% 10%, 70% 0%, 100% 0%, 100% 70%, 0% 70%);
  }

  .petal.top {
    transform: rotateZ(0deg);
  }
  .petal.up-right {
    transform: rotateZ(72deg);
  }
  .petal.down-right {
    transform: rotateZ(144deg);
  }
  .petal.down-left {
    transform: rotateZ(-144deg);
  }
  .petal.up-left {
    transform: rotateZ(-72deg);
  }

  .sepal {
    position: absolute;
    top: 39%;
    left: 36%;
    width: 20%;
    height: 20%;
  }

  .light {
    background-color: pink;
  }
  .dark {
    background-color: magenta;
  }

  .border {
    transform: scale(1.1);
  }
  .border .petal > div {
    background-color: #444;
  }
</style>
