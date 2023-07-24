<template>
  <suspense>
    <template #default>
      <Home></Home>
    </template>
    <template #fallback>
      <SplashScreeen></SplashScreeen>
    </template>
  </suspense>
</template>

<script>
import SplashScreeen from "@/components/SplashScreeen.vue";
import { defineAsyncComponent } from "vue";

export default {
  components: {
    SplashScreeen,
    Home: defineAsyncComponent(
      () =>
        new Promise((resolve) => {
          setTimeout(() => {
            resolve(import("./components/Home.vue"));
          }, 2500);
        })
    ),
  },
};
</script>

<style>
html,
body,
.app {
  min-height: 100vh;
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
}
* {
  --brand-green: #04b500;
  --brand-blue: #0689b0;
}
</style>
