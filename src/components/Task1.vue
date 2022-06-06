<template>
  <div class="container">
    <h1 class="title__singleInputs">{{ firstCharUpper(titleOne) }}</h1>
    <div class="box">
      <form class="form__singleInput" @submit.prevent="changeTitleOne()">
        <input
          class="input__singleInput"
          type="text"
          v-model="inputValueOne"
          placeholder="Update title..."
          autofocus
          required="required"
        />
        <button class="button">Change</button>
      </form>
    </div>
  </div>
</template>

<style lang="scss">
@import "../styles/SingleInputs.scss";
</style>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "TaskOne",
  data: () => ({
    inputValueOne: "",
    titleOne: "Title",
  }),
  methods: {
    firstCharUpper(str: string) {
      return str.charAt(0).toUpperCase() + str.slice(1);
    },
    changeTitleOne() {
      this.titleOne = this.inputValueOne;
      this.inputValueOne = "";
    },
  },
});
</script>
