<template>
  <div class="ui segment" :class="{raised: isRaised}" @mouseover="itemMouseOver" @mouseleave="itemMouseLeave">
    <div class="ui items">
      <div class="ui item">
        <div class="content">
          <a class="ui teal left ribbon label">to Look</a>
          <div class="ui huge header">
            <a>{{ item.title }}</a>
          </div>
          <div class="meta">
            <div class="ui basic label ">
              <i class="user circle outline icon"></i>
              <a href="#">{{ item.authorName }}</a>
            </div>
            <div class="ui basic label">
              <i class="calendar alternate outline icon"></i>
              <span>{{ item.date }}</span>
            </div>
          </div>
          <div class="description">
            <p>{{ item.descrption }}</p>
          </div>
          <div class="extra">
            <div class="ui left floated">
              <div class="ui labeled button" tabindex="0">
                <div class="ui button">
                  <i class="heart outline icon"></i> Like
                </div>
                <a class="ui basic label">
                  {{ item.likes }}
                </a>
              </div>
              <div class="ui labeled button" tabindex="0">
                <div class="ui icon button">
                  <i class="chart line icon"></i> Viewed
                </div>
                <a class="ui basic label">
                  {{ item.views }}
                </a>
              </div>
            </div>
            <div class="ui right floated">
              <i class="big chevron circle right link icon"></i>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "BlogItem",
  data() {
    return {
      isRaised: true
    }
  },
  props: {
    item:{
      default() {
        return {
        }
      }
    },
  },
  methods: {

    // 绑定鼠标悬停-离开事件(变化抬起放下)
    itemMouseOver() {
      this.$data.isRaised = false
    },
    itemMouseLeave() {
      this.$data.isRaised = true
    }
  }
}
</script>

<style scoped>

</style>