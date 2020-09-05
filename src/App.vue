<template>
  <div id="app">
    <TabBar />
    <router-view />
  </div>
</template>

<script>
import TabBar from "@/components/tabbar/TabBar";
export default {
  name: "app",
  components: {
    TabBar,
  },
};
</script>

<style>

</style>
