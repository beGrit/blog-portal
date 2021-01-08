<template>
  <div>
    <top-navbar></top-navbar>
    <router-view></router-view>
  </div>
</template>

<script>
import TopNavbar from "@/views/layout/components/TopNavbar";
export default {
  name: "Layout",
  components: {TopNavbar}
}
</script>

<style scoped>

</style>