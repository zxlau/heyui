<style lang="less">
</style>

<template>
  <div v-bg-color:gray4 v-padding="20">
    <Menu :datas="data" mode="horizontal" @select="triggerSelect"></Menu>
  </div>
</template>

<script>
export default {
  data() {
    return {
      data: [
        {
          title: '首页',
          key: 'welcome',
          icon: 'h-icon-home'
        },
        {
          title: '查询',
          key: 'search',
          icon: 'h-icon-search'
        },
        {
          title: '收藏',
          key: 'favor',
          icon: 'h-icon-star',
          children: [
            {
              title: '类型-1',
              key: '2-1'
            },
            {
              title: '类型-2',
              key: '3-2',
              children: [
                {
                  title: '类型-2-3',
                  key: '2-3'
                },
                {
                  title: '类型-2-4',
                  key: '3-4'
                }
              ]
            }
          ]
        },
        {
          title: '任务',
          icon: 'h-icon-task',
          key: 'task',
          children: [
            {
              title: '模块1-1',
              icon: 'h-icon-bell',
              key: '1-1'
            },
            {
              title: '模块1-2',
              icon: 'h-icon-home',
              key: '1-2'
            }
          ]
        }
      ]
    };
  },
  methods: {
    triggerSelect(menu) {
      this.$Message.info(`选中${menu.title}`);
    }
  }
};
</script>