<template>
  <div v-if="menu_data">
    <template v-for="submenu of menu_data">
      <el-submenu :index="submenu.index">
        <template slot="title">
          <i class="el-icon-location"></i>
          <span slot="title">{{ submenu.title }}</span>
        </template>
        <template v-for="item of submenu.items">
          <el-menu-item :index="item.index">
            {{ item.title }}
          </el-menu-item>
        </template>
          <template v-if="submenu.submenu.length>0">
            <auto-sub-menu :subMenuData="submenu.submenu">
            </auto-sub-menu>
          </template>
      </el-submenu>
    </template>
  </div>
</template>
<style scoped>
</style>
<script>
export default {
  name: 'AutoSubMenu',
  props: ['subMenuData'],
  data () {
    return {
      menu_data: this.subMenuData
    }
  },
  mounted () {
    console.log(this.menu_data)
  }
}
</script>
