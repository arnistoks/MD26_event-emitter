<template>
  <div class="container__boxHide">
    <h1 class="title__singleInputs">Show or hide cube</h1>
    <div class="result__cubeHide">
      <div class="box__cubeHide">
        <h5 class="comment">
          {{ !hiddenCubeOne ? "Show cube" : "Hide cube" }}
        </h5>
        <button class="button" @click="hideCubeOne()">Change</button>
      </div>
      <div
        class="cube"
        :style="{ display: !hiddenCubeOne ? 'none' : 'block' }"
      />
    </div>
  </div>
</template>

<style lang="scss">
@import "../styles/DoubleInputs.scss";
</style>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "TaskSeven",
  data: () => ({
    hiddenCubeOne: true,
  }),
  methods: {
    hideCubeOne() {
      this.hiddenCubeOne = !this.hiddenCubeOne;
    },
  },
});
</script>
