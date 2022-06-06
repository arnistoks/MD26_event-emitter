<template>
  <div class="container">
    <h1 class="title__singleInputs">{{ firstCharUpper(titleOne) }}</h1>
    <div class="box">
      <Form1 @changeTitleOne="changeTitleOne" />
    </div>
  </div>
</template>

<style lang="scss">
@import "../styles/SingleInputs.scss";
</style>

<script lang="ts">
import { defineComponent } from "vue";
import Form1 from "../components/Form1.vue";

export default defineComponent({
  name: "TaskOne",
  components: {
    Form1,
  },
  data: () => ({
    inputValueOne: "",
    titleOne: "Title",
  }),
  methods: {
    firstCharUpper(str: string) {
      return str.charAt(0).toUpperCase() + str.slice(1);
    },
    changeTitleOne(title: string) {
      this.titleOne = title;
    },
  },
});
</script>
