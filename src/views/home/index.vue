<template>
  <div class="ui grid">
    <div class="eleven wide column">
      <blog-content></blog-content>
    </div>
    <div class="five wide column">
      <blog-side-nav></blog-side-nav>
    </div>
  </div>
</template>

<script>
import BlogContent from "@/views/home/components/BlogContent";
import BlogSideNav from "@/views/home/components/BlogRightNav";

export default {
  name: "index",
  components: {
    BlogContent,
    BlogSideNav
  }
}
</script>

<style scoped/>