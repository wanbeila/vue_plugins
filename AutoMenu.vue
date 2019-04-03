<template>
  <el-menu-item-group>
    <span
      class="group-title"
      slot="title"
    >{{ menu_data.group_title }}</span>
    <!-- 如果菜单数据中的子菜单不为空 -->
    <template v-if="menu_data.submenu.length>0">
      <auto-submenu :subMenuData="menu_data.submenu"></auto-submenu>
    </template>
    <!-- <template v-else-if="menu_data.items.length == 0">
        <template v-for="item of menu_data.items">
          <el-menu-item index="item.index">
            {{ item.title }}
          </el-menu-item>
        </template>
    </template> -->
  </el-menu-item-group>
</template>
<style scoped>
</style>
<script>
import AutoSubmenu from '@/pages/components/AutoSubmenu'
export default {
  components: {
    AutoSubmenu
  },
  name: 'AutoMenu',
  props: ['groupMenuData'],
  data () {
    return {
      menu_data: this.groupMenuData
    }
  },
  mounted() {
    // console.log(this.menu_data)
  }
}
</script>
