<template>
  <div class="layout" >
    <Layout :style="{minHeight: '93vh'}">
      <Sider collapsible :collapsed-width="78" v-model="isCollapsed" >
        <Menu active-name="1-2" theme="dark" width="auto" :open-names="['1']">
          <Submenu name="1">
            <template slot="title">
              <Icon type="ios-car" />
              车辆白名单
            </template>
            <MenuItem name="1-1">机动车</MenuItem>
            <MenuItem name="1-2">三轮车</MenuItem>
            <MenuItem name="1-3">内部车</MenuItem>
          </Submenu>
          <Submenu name="2">
            <template slot="title">
              <Icon type="md-menu" />
              通行记录
            </template>
            <MenuItem name="2-1">机动车</MenuItem>
            <MenuItem name="2-2">三轮车</MenuItem>
            <MenuItem name="2-2">内部车</MenuItem>
          </Submenu>
          <Submenu name="3">
            <template slot="title">
              <Icon type="ios-information-circle" />
              停车信息
            </template>
            <MenuItem name="3-1">车位信息</MenuItem>
            <MenuItem name="3-2">停车时长</MenuItem>
          </Submenu>
          <Submenu name="4">
            <template slot="title">
              <Icon type="logo-yen" />
              缴费信息
            </template>
            <MenuItem name="4-1">缴费明细</MenuItem>
            <MenuItem name="4-2">缴费统计</MenuItem>
          </Submenu>
          <MenuItem name="5">
            <Icon type="ios-remove-circle-outline" />
            <span>黑名单</span>
          </MenuItem>
          <MenuItem name="6">
            <Icon type="md-person" />
            <span>管理员</span>
          </MenuItem>
        </Menu>
      </Sider>
      <Layout :style="{padding: '0px 16px 5px 16px'}">
        <Content :style="{padding: '12px', minHeight: '280px', background: '#fff',marginTop: '20px'}">
          Content
        </Content>
        <Footer class="layout-footer-center">skeleton by Xansux</Footer>
      </Layout>
    </Layout>
  </div>
</template>
<style scoped>
  .layout-con{
    height: 100%;
    width: 100%;
  }
  .menu-item span{
    display: inline-block;
    overflow: hidden;
    /*display: inline-block;*/
    width: 69px;
    text-overflow: ellipsis;
    white-space: nowrap;
    vertical-align: bottom;
    transition: width .2s ease .2s;
  }
  .menu-item i{
    transform: translateX(0px);
    transition: font-size .2s ease, transform .2s ease;
    vertical-align: middle;
    font-size: 16px;
  }
  .collapsed-menu span{
    width: 0px;
    transition: width .2s ease;
  }
  .collapsed-menu i{
    transform: translateX(5px);
    transition: font-size .2s ease .2s, transform .2s ease .2s;
    vertical-align: middle;
    font-size: 22px;
  }
  .ivu-layout-footer{
    padding: 0;
    margin-top: 12px;
    text-align: right;
  }
</style>
<script>
  export default {
    data () {
      return {
        isCollapsed: false
      };
    },
    computed: {
      menuitemClasses: function () {
        return [
          'menu-item',
          this.isCollapsed ? 'collapsed-menu' : ''
        ]
      }
    }
  }
</script>
