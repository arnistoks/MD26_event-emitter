<template>
  <input
    class="input__singleInput"
    type="text"
    v-model="inputValueTwo"
    placeholder="Update title..."
    required="required"
    @change="SubmitHandler"
  />
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "FormTwo",
  emits: ["changeTitleTwo"],
  data() {
    return {
      inputValueTwo: "",
    };
  },
  methods: {
    SubmitHandler() {
      this.$emit("changeTitleTwo", this.inputValueTwo);

      this.inputValueTwo = "";
    },
  },
});
</script>
