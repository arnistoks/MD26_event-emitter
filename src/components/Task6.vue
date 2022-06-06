<template>
  <div class="container__doubleInputs">
    <div class="box__doubleInputs">
      <form class="form__singleInput" @input.prevent="changeTitleTwo()">
        <input
          class="input__singleInput"
          type="text"
          v-model="inputValueTitleTwo"
          placeholder="Update title..."
          required="required"
        />
      </form>
      <form class="form__singleInput" @input.prevent="changeDescriptionTwo()">
        <input
          class="input__singleInput"
          type="text"
          v-model="inputValueDescriptionTwo"
          placeholder="Update description..."
          required="required"
        />
      </form>
    </div>
    <div class="text__box">
      <h1 class="title__doubleInputs">{{ firstCharUpper(titleTwo) }}</h1>
      <p class="description__doubleInputs">
        {{ firstCharUpper(descriptionTwo) }}
      </p>
    </div>
  </div>
</template>

<style lang="scss">
@import "../styles/DoubleInputs.scss";
</style>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "TaskSix",
  data: () => ({
    inputValueTitleTwo: "",
    titleTwo: "Title",
    inputValueDescriptionTwo: "",
    descriptionTwo: "Description",
  }),
  methods: {
    firstCharUpper(str: string) {
      return str.charAt(0).toUpperCase() + str.slice(1);
    },
    changeTitleTwo() {
      this.titleTwo = this.inputValueTitleTwo;
    },
    changeDescriptionTwo() {
      this.descriptionTwo = this.inputValueDescriptionTwo;
    },
  },
});
</script>
