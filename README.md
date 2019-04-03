# vue_plugins
element-ui动态导航菜单
菜单按组来分，如需用到多个分组可以通过传入的数组进行遍历创建

Test.vue为使用的例子


数据格式
```javascript
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
```

![preview](https://github.com/wanbeila/vue_plugins/blob/master/example.png)
![preview2](https://github.com/wanbeila/vue_plugins/blob/master/example2.png)
