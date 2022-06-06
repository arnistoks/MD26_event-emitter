<template>
  <div class="container">
    <h1 class="title__singleInputs">Color change</h1>
    <div class="result__row">
      <div class="box__color">
        <form class="form__singleInput" @submit.prevent="changeCubeColorOne()">
          <input
            class="input__singleInput"
            type="text"
            v-model="inputValueCubeColorOne"
            placeholder="Change color..."
            autofocus
            required="required"
          />
          <button class="button">Change</button>
        </form>
      </div>
      <div class="cube" :style="cubeColorOne" />
    </div>
  </div>
</template>

<style lang="scss">
@import "../styles/SingleInputs.scss";
</style>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "TaskThree",
  data: () => ({
    inputValueCubeColorOne: "",
    cubeColorOne: {
      backgroundColor: "Blue",
    },
  }),
  methods: {
    changeCubeColorOne() {
      this.cubeColorOne.backgroundColor = this.inputValueCubeColorOne;
      this.inputValueCubeColorOne = "";
    },
  },
});
</script>
