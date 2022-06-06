<template>
  <div class="container">
    <h1 class="title__singleInputs">Color change</h1>
    <div class="result__row">
      <div class="box__color">
        <form class="form__singleInput" @input.prevent="changeCubeColorTwo()">
          <input
            class="input__singleInput"
            type="text"
            v-model="inputValueCubeColorTwo"
            placeholder="Change color..."
            autofocus
            required="required"
          />
        </form>
      </div>
      <div class="cube" :style="cubeColorTwo" />
    </div>
  </div>
</template>

<style lang="scss">
@import "../styles/SingleInputs.scss";
</style>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "TaskFour",
  data: () => ({
    inputValueCubeColorTwo: "",
    cubeColorTwo: {
      backgroundColor: "Blue",
    },
  }),
  methods: {
    changeCubeColorTwo() {
      this.cubeColorTwo.backgroundColor = this.inputValueCubeColorTwo;
    },
  },
});
</script>
