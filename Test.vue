<template>
  <el-menu
    :default-active="$route.path"
    class="el-menu-vertical-demo"
    :collapse="isCollapse"
    router
    @open="handleOpen"
    @close="handleClose"
  >
    <auto-menu :groupMenuData="group_menu"></auto-menu>
  </el-menu>
</template>
<script>
import AutoMenu from '@/pages/components/AutoMenu'
export default {
  components: {
    AutoMenu
  },
  methods: {
    handleOpen (key, keyPath) {
      // console.log(key, keyPath);
    },
    handleClose (key, keyPath) {
      // console.log(key, keyPath);
    },
  },
  data () {
    return {
      isCollapse: false,
      group_menu: {
        group_title: 'analyzer',
        submenu: [
          {
            index: '/reporting',
            title: 'Reporting',
            items: [
              {
                index: '/kpi_pi',
                title: 'KPI/PI'
              },
              {
                index: '/shift_handover',
                title: 'ShiftHandover'
              },
              {
                index: '/batch_process_parameter_report',
                title: 'Batch Process Parameter Report'
              },
              {
                index: '/messasge_report',
                title: 'Message Report'
              }
            ],
            submenu: [
              {
                index: '/lab_data_report',
                title: 'Lab Data Report',
                items: [
                  {
                    index: '/raw_material',
                    title: 'Raw Material'
                  },
                  {
                    index: '/process_indicator',
                    title: 'Process Indicator'
                  },
                  {
                    index: '/finish_goods',
                    title: 'Finish Goods'
                  },
                  {
                    index: '/bwc',
                    title: 'BWC'
                  }
                ],
                submenu: []
              }
            ]
          },
          {
            index: '/dashboard',
            title: 'Dashboard',
            items: [
              {
                index: '/spc',
                title: 'SPC'
              },
              {
                index: '/dot_graph',
                title: 'Dot Graph'
              },
              {
                index: '/benchmark',
                title: 'Benchmark'
              }
            ],
            submenu: []
          }
        ]
      }
    }
  }
}
</script>
