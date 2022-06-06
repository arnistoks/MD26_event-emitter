<template>
  <div class="container__boxHide">
    <h1 class="title__singleInputs">Show or hide cube</h1>
    <div class="result__cubeHide">
      <div class="box__cubeHide">
        <label class="label" for="checkbox">
          <h5 class="comment">
            {{ !hiddenCubeTwo ? "Show cube" : "Hide cube" }}
          </h5>
          <input type="checkbox" name="checkboxOne" v-model="hiddenCubeTwo" />
        </label>
      </div>
      <div
        class="cube"
        :style="{ display: !hiddenCubeTwo ? 'none' : 'block' }"
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
  name: "TaskEight",
  data: () => ({
    hiddenCubeTwo: true,
  }),
});
</script>
