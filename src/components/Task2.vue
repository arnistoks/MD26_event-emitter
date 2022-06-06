<template>
  <div class="container">
    <h1 class="title__singleInputs">{{ firstCharUpper(titleTwo) }}</h1>
    <div class="box">
      <Form2 @changeTitleTwo="changeTitleTwo" />
      <!--      <form class="form__singleInput" @input.prevent="changeTitleTwo()">-->
      <!--        <input-->
      <!--          class="input__singleInput"-->
      <!--          type="text"-->
      <!--          v-model="inputValueTwo"-->
      <!--          placeholder="Update title..."-->
      <!--          required="required"-->
      <!--        />-->
      <!--      </form>-->
    </div>
  </div>
</template>

<style lang="scss">
@import "../styles/SingleInputs.scss";
</style>

<script lang="ts">
import { defineComponent } from "vue";
import Form2 from "../components/Form2.vue";

export default defineComponent({
  name: "TaskTwo",
  components: {
    Form2,
  },
  data: () => ({
    inputValueTwo: "",
    titleTwo: "Title",
  }),
  methods: {
    firstCharUpper(str: string) {
      return str.charAt(0).toUpperCase() + str.slice(1);
    },
    changeTitleTwo(title: string) {
      this.titleTwo = title;
    },
  },
});
</script>
