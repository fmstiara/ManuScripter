<template>
  <div id="sidemenu">
    <el-menu>
      <el-menu-item index="1" v-on:click="create()">
        <i class="el-icon-edit"></i>
        <span>原稿作成</span>
      </el-menu-item>
      <el-menu-item index="2" v-on:click="index()">
        <i class="el-icon-menu"></i>
        <span>原稿一覧</span>
      </el-menu-item>
    </el-menu>
  </div>
</template>

<script>
export default {
  name: 'SideMenu',
  methods: {
    create: function () {
      this.$router.push('edit')
    },
    index: function () {
      this.$router.push('index')
    }
  }
}
</script>
