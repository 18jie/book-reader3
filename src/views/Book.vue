<template>
  <div>
    <el-row class="grid-content bg-purple-light">
      <el-link class="login-link"
               href="https://element.eleme.io"
               target="_blank">注册</el-link>
      |
      <el-link href="https://element.eleme.io"
               target="_blank">登录</el-link>
    </el-row>
    <el-row class="search-row">
      <el-col :span="5">
        <el-image style="width: 100px; height: 100px"
                  :src="url"
                  :fit="fit"></el-image>
      </el-col>
      <el-col :span="6"
              :offset="1">
        <el-input size="normal"
                  v-model="search"
                  placeholder="请输入内容"></el-input>
      </el-col>
      <el-col :span="1">
        <el-button size="normal"
                   icon="el-icon-search"
                   circle
                   class="float:right;"
                   @click="searchMethod"></el-button>
      </el-col>
    </el-row>
    <el-menu :default-active="activeIndex2"
             class="el-menu-demo"
             mode="horizontal"
             @select="handleSelect"
             background-color="#545c64"
             text-color="#fff"
             active-text-color="#ffd04b">
      <el-menu-item index="1">处理中心</el-menu-item>
      <el-submenu index="2">
        <template slot="title">我的工作台</template>
        <el-menu-item index="2-1">选项1</el-menu-item>
        <el-menu-item index="2-2">选项2</el-menu-item>
        <el-menu-item index="2-3">选项3</el-menu-item>
        <el-submenu index="2-4">
          <template slot="title">选项4</template>
          <el-menu-item index="2-4-1">选项1</el-menu-item>
          <el-menu-item index="2-4-2">选项2</el-menu-item>
          <el-menu-item index="2-4-3">选项3</el-menu-item>
        </el-submenu>
      </el-submenu>
      <el-menu-item index="3"
                    disabled>消息中心</el-menu-item>
      <el-menu-item index="4"><a href="https://www.ele.me"
           target="_blank">订单管理</a></el-menu-item>
    </el-menu>
    <div class="main-part">
      <div class="left-part">111</div>
      <el-carousel height="150px">
        <el-carousel-item v-for="item in 4"
                          :key="item">
          <h3 class="small">{{ item }}</h3>
        </el-carousel-item>
      </el-carousel>
      <div class="right-part">111</div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.el-row {
  margin-bottom: 5px;
  &:last-child {
    margin-bottom: 0;
  }
}
.el-col {
  border-radius: 4px;
}
.bg-purple-dark {
  background: #99a9bf;
}
.bg-purple {
  background: #d3dce6;
}
.bg-purple-light {
  background: #e5e9f2;
}
.grid-content {
  border-radius: 4px;
  min-height: 36px;
}
.row-bg {
  padding: 10px 0;
  background-color: #f9fafc;
}
.el-menu {
  padding-left: 35%;
}
.login-link {
  margin-left: 80%;
  // float:right;
}

// 主要部分css
.main-part {
  padding-left: 10%;
  padding-right: 10%;
}

// 搜索部分
.search-row {
  height: 80px;
}

// 左侧部分
.left-part {
  background-color: black;
  height: 100px;
  width: 300px;
  float: left;
}
// 右侧部分
.right-part {
  background-color: black;
  height: 100px;
  width: 300px;
  position: absolute;
  top: 110px;
  left: 69.6%;
}

// 走马灯css
.el-carousel {
  width: 50%;
}
.el-carousel__item h3 {
  color: #475669;
  font-size: 14px;
  opacity: 0.75;
  line-height: 150px;
  margin: 0;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d3dce6;
}
</style>>