<template>
  <div>
    <!--头部区-->
    <div class="ui top segment">
      <div class="ui middle aligned two column grid">
        <div class="left aligned column">
          <h3 class="ui teal header">博客</h3>
        </div>
        <div class="right aligned column">
          <span>
            共<h3 class="ui orange header" style="display: inline-block">{{ total }}</h3>篇
          </span>
        </div>
      </div>
    </div>
    <!--内容区-->
    <div class="ui tow column grid segment">
      <div v-for="item in list" class="eight wide column">
        <blog-item :item="item"></blog-item>
      </div>
    </div>
    <!-- 底部区 -->
    <div class="ui bottom attached segment">
      <div class="ui middle aligned two column grid">
        <div class="column">
          <a href="#" class="ui mini green basic button">上一页</a>
        </div>
        <div class="right aligned column">
          　　<a href="#" class="ui mini red basic button">下一页</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import BlogItem from "@/components/BlogItem";
import PlaceHolderItem from "@/components/PlaceHolderItem";

let myJson = {
  'total': 100,
  'pageSize': 10,
  'pageNum': 1,
  'list': [
    {
      'title': 'Scrapy教程',
      'authorName': 'Pocky',
      'date': '2021-01-05',
      'descrption': 'asdasdas',
      'likes': 1000,
      'views': 2000,
    },
    {
      'title': 'Python教程',
      'authorName': 'Pocky',
      'date': '2021-01-05',
      'descrption': 'python.....',
      'likes': 20,
      'views': 1010,
    },
    {
      'title': 'Java教程',
      'authorName': 'Pocky',
      'date': '2021-01-05',
      'descrption': 'asdas',
      'likes': 20,
      'views': 1010,
    },
  ]
}


export default {
  name: "BlogContent",
  components: {PlaceHolderItem, BlogItem},
  data() {
    return {
      total: myJson.total,
      pageSize: myJson.pageSize,
      pageNum: myJson.pageNum,
      list: myJson.list,
    }
  },
  created() {

  },
  methods: {
    getList() {

    },
  }
}

</script>

<style scoped>

</style>