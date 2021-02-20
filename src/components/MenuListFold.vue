<template>
    <transition>
         <el-menu
      default-active="2"
      class="el-menu-vertical-demo"
      @open="handleOpen"
      @close="handleClose"
      :router=true
      background-color="rgb(0,21,41)"
      text-color="#fff"
      active-text-color="green">
      <el-submenu index="/Home">
        <template slot="title">
          <i class="el-icon-menu"></i>
        </template>
          <el-menu-item index="/Home/total" icon='el-icon-view'>统计</el-menu-item>
      </el-submenu>
      <el-submenu index="/goods">
          <template slot="title">
        <i class="el-icon-s-goods"></i>
          </template>
        <el-menu-item index="/goods/lists" >商品列表</el-menu-item>
         <el-menu-item index="/goods/add" >添加商品</el-menu-item>
      </el-submenu>
    </el-menu>
    </transition>

</template>
<style scoped>
  el-menu-item{
    width: 100px;
  }
  .v-enter {
  opacity: 0;
}

/* .v-enter-active {

} */

.v-enter-to {
  opacity: 1;
}

.v-leave {
  opacity: 1;
}

/* .v-leave-active {

} */

.v-leave-to {
  opacity: 0;
}

</style>
