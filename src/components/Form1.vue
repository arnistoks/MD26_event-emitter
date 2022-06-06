<template>
  <form class="form__singleInput" @submit.prevent="SubmitHandler">
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
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "FormOne",
  emits: ["changeTitleOne"],
  data() {
    return {
      inputValueOne: "",
    };
  },
  methods: {
    SubmitHandler() {
      this.$emit("changeTitleOne", this.inputValueOne);

      this.inputValueOne = "";
    },
  },
});
</script>
