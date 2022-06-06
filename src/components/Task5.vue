<template>
  <div class="container__doubleInputs">
    <div class="box__doubleInputs">
      <form class="form__singleInput" @submit.prevent="changeTitleOne()">
        <input
          class="input__singleInput"
          type="text"
          v-model="inputValueTitleOne"
          placeholder="Update title..."
          autofocus
          required="required"
        />
        <button class="button">Change</button>
      </form>
      <form class="form__singleInput" @submit.prevent="changeDescriptionOne()">
        <input
          class="input__singleInput"
          type="text"
          v-model="inputValueDescriptionOne"
          placeholder="Update description..."
          autofocus
          required="required"
        />
        <button class="button">Change</button>
      </form>
    </div>
    <div class="text__box">
      <h1 class="title__doubleInputs">{{ firstCharUpper(titleOne) }}</h1>
      <p class="description__doubleInputs">
        {{ firstCharUpper(descriptionOne) }}
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
  name: "TaskFive",
  data: () => ({
    inputValueTitleOne: "",
    titleOne: "Title",
    inputValueDescriptionOne: "",
    descriptionOne: "Description",
  }),
  methods: {
    firstCharUpper(str: string) {
      return str.charAt(0).toUpperCase() + str.slice(1);
    },
    changeTitleOne() {
      this.titleOne = this.inputValueTitleOne;
      this.inputValueTitleOne = "";
    },
    changeDescriptionOne() {
      this.descriptionOne = this.inputValueDescriptionOne;
      this.inputValueDescriptionOne = "";
    },
  },
});
</script>
