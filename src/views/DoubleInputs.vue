<template>
  <section class="section">
    <Task5 />
    <Task6 />
    <Task7 />
    <Task8 />
  </section>
</template>

<style lang="scss">
@import "../styles/DoubleInputs.scss";
</style>

<script lang="ts">
import { defineComponent } from "vue";
import Task5 from "../components/Task5.vue";
import Task6 from "../components/Task6.vue";
import Task7 from "../components/Task7.vue";
import Task8 from "../components/Task8.vue";

export default defineComponent({
  name: "DoubleInputs",
  components: {
    Task5,
    Task6,
    Task7,
    Task8,
  },
});
</script>
