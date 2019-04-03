# vue_plugins
element-ui动态导航菜单
菜单按组来分，如需用到多个分组可以通过传入的数组进行遍历创建

Test.vue为使用的例子


数据格式
```javascript
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
```

![preview](https://github.com/wanbeila/vue_plugins/blob/master/example.png)
![preview2](https://github.com/wanbeila/vue_plugins/blob/master/example2.png)
