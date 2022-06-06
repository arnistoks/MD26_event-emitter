<template>
  <section class="section">
    <Task1 />
    <Task2 />
    <Task3 />
    <Task4 />
  </section>
</template>

<style lang="scss">
@import "../styles/SingleInputs.scss";
</style>

<script lang="ts">
import { defineComponent } from "vue";
import Task1 from "../components/Task1.vue";
import Task2 from "../components/Task2.vue";
import Task3 from "../components/Task3.vue";
import Task4 from "../components/Task4.vue";

export default defineComponent({
  name: "SingleInputs",
  components: {
    Task1,
    Task2,
    Task3,
    Task4,
  },
});
</script>
