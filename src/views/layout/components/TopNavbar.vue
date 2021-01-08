<template>
  <div>
    <nav>
      <div class="ui inverted pointing stackable menu">
        <a href="#" class="ui green header item">博客</a>
        <a href="#" class="blue item"><i class="home icon"></i>首页</a>
        <a href="#" class="orange item"><i class="idea icon"></i>分类</a>
        <a href="#" class="yellow item"><i class="tags icon"></i>标签</a>
        <a href="#" class="green item"><i class="info icon"></i>关于我</a>
        <div class="right item">
          <div class="ui icon inverted transparent input">
            <input type="text" placeholder="Search...">
            <i class="search link icon"></i>
          </div>
        </div>
      </div>
    </nav>
  </div>
</template>
<script>
  export default {
    name: 'TopNavbar',
  }
</script>
<style></style>