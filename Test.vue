<template>
  <el-menu
    :default-active="$route.path"
    class="el-menu-vertical-demo"
    :collapse="isCollapse"
    router
    @open="handleOpen"
    @close="handleClose"
  >
    <template v-for="group_menu of menu_data">
      <auto-menu :groupMenuData="group_menu.group_menu"></auto-menu>
    </template>
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
      menu_data: [{
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
          ],
          items: []
        }
      },
      {
        group_menu: {
          group_title: 'Tracking',
          submenu: [],
          items: [
            {
              index: '/batch_parameter',
              title: 'Batch Parameter'
            },
            {
              index: '/sampling_process',
              title: 'Sampling Process'
            },
            {
              index: '/kpi_pi',
              title: 'KPI/PI'
            },
            {
              index: '/gops_bpe',
              title: 'GOPS/BPE'
            }
          ]
        }
      },
      {
        group_menu: {
          group_title: 'Lab Operation',
          submenu: [],
          items: [
            {
              index: '/certification',
              title: 'Certification'
            },
            {
              index: '/calibration',
              title: 'Calibration'
            },
            {
              index: '/reagent',
              title: 'Reagent'
            },
            {
              index: '/sop_opl',
              title: 'SOP/OPL'
            },
            {
              index: '/fabric',
              title: 'Fabric'
            }
          ]
        }
      },

      {
        group_menu: {
          group_title: 'System Configuration',
          submenu: [],
          items: [
            {
              index: '/physical_modeling',
              title: 'Physical Modeling'
            },
            {
              index: '/process_modeling',
              title: 'Process Modeling'
            },
            {
              index: '/sampling',
              title: 'Sampling'
            },
            {
              index: '/pts',
              title: 'PTS'
            },
            {
              index: '/data_acquisition',
              title: 'Data Acquisition'
            },
            {
              index: '/user',
              title: 'User'
            }
          ]
        }
      }
      ]
    }
  }
}
</script>
