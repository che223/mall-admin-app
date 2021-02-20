<template>
  <div class="home">
    <div :class="{'menu-list':true,'menu-fold':collasped}">
      <menulist v-if="!collasped" class="unfold"></menulist>
      <menulist-fold v-if="collasped" class="fold"></menulist-fold>
    </div>
    <div :class="{'main-app':true,'menu-fold':collasped}">
     <el-button
      type="success"
      icon="el-icon-s-fold"
      style="margin-left:16px"
      @click="toggleCollapsed"
      ></el-button>
      <div class="breadcrumb">
        <breadcrumb></breadcrumb>
      </div>
      <div class="userInfo">
        用户信息
      </div>
    </div>
  </div>
</template>
<script>
import Menulist from '../../components/MenuList.vue';
import MenulistFold from '../../components/MenuListFold.vue';
import Breadcrumb from '../../components/Breadcrumb.vue';

export default {
  data() {
    return {
      collasped: false,
    };
  },
  components: {
    Menulist,
    Breadcrumb,
    MenulistFold,

  },
  methods: {
    toggleCollapsed() {
      this.collasped = !this.collasped;
    },
  },
};
</script>
<style lang='less'>
@import url('~@/assets/css/Home.less');
</style>
