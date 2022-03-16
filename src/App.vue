<script>
import ChangeImgVue from "./components/ChangeImg.vue";
import RouterSumVue from "./components/RouterSum.vue";

const routes = {
  "/": ChangeImgVue,
  "/routersum": RouterSumVue,
};

export default {
  data() {
    return {
      currentPath: window.location.hash,
    };
  },
  computed: {
    currentView() {
      return routes[this.currentPath.slice(1) || "/"];
    },
  },
  mounted() {
    window.addEventListener("hashchange", () => {
      this.currentPath = window.location.hash;
    });
  },
};
</script>

<template>
  <a href="#/">Change Image</a>
  <a href="#/routersum">Router Sum</a>
  <component :is="currentView" />
</template>

<style>
a {
  display: block;
  width: 60px;
  background-color: #dddddd;
}
</style>
