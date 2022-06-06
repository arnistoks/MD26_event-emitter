<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/singleInputs">Single inputs</router-link> |
    <router-link to="/doubleInputs">Double inputs</router-link>
  </nav>
  <router-view />
</template>

<style lang="scss">
@import "./styles/App.scss";
</style>
