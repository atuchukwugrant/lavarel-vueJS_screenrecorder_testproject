<template>
  <div id="app">
    <TopMenu />
    <AppSidebar />
    
  </div>
</template>

<script>
import AppSidebar from "./components/AppSidebar.vue";
import TopMenu from "@/components/TopMenu.vue";

export default {
  name: 'App',
  components: {
    AppSidebar, TopMenu,
  }
}
</script>

<style>

</style>

