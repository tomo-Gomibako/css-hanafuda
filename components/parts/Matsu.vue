<template>
  <div class="matsu">
    <div class="leaves center">
      <div class="texture" />
      <div class="texture v-flip" />
    </div>
    <div class="left-leaves-container">
      <div class="leaves left">
        <div class="texture" />
        <div class="texture v-flip" />
      </div>
    </div>
    <div class="left-leaves-container v-flip">
      <div class="leaves left">
        <div class="texture" />
        <div class="texture v-flip" />
      </div>
    </div>
  </div>
</template>

<style scoped>
  .matsu {
    width: 100%;
    height: 100%;
  }
  .matsu::before {
    content: '';
    position: absolute;
    width: 100%;
    height: 100%;
    clip-path: ellipse(2% 2.5% at 50% 30%);
    background-color: yellow;
    z-index: 1;
  }

  .matsu .leaves {
    display: flex;
    position: absolute;
    bottom: 0;
    width: 100%;
    height: 100%;
  }
  .leaves.center {
    clip-path: ellipse(20% 40% at 50% 70%);
  }
  .leaves.center > .texture {
    width: 50%;
    height: 100%;
    background: repeating-linear-gradient(40deg, black, black 2px, #252525 5px, #252525 10px);
  }

  .left-leaves-container {
    position: absolute;
    width: 100%;
    height: 100%;
    clip-path: polygon(0% 0%, 50% 0%, 50% 100%, 0% 100%);
  }
  .leaves.left {
    clip-path: ellipse(18% 40% at 50% 50%);
    transform: translate(5%, 52%) rotateZ(-45deg);
  }
  .leaves.left > .texture {
    width: 50%;
    height: 100%;
    background: repeating-linear-gradient(40deg, black, black 2px, #252525 5px, #252525 10px);
  }
  .left-leaves-container::before {
    content: '';
    position: absolute;
    width: 100%;
    height: 100%;
    /* width: 10%;
    height: 10%;
    top: 70%;
    left: 5%; */
    /* clip-path: ellipse(2% 2.5% at 9% 74%); */
    clip-path: ellipse(2% 2.5% at 50% 10%);
    transform: translate(5%, 52%) rotateZ(-45deg);
    background-color: yellow;
    z-index: 1;
  }

  .v-flip {
    transform: scaleX(-1);
  }
</style>
