<template>
  <div>
    <m-header title="豆瓣app" :bg="true">
      <a href="javascript:;" slot="left">< img class="m-icon-img" src="../../assets/images/ic_bar_back_white.png"/>返回</a>
      <a href="javascript:;" slot="right">分享</a>
    </m-header>
    <m-header title="豆瓣app" :bg="true">
      <a href="javascript:;" slot="left">< img class="m-icon-img" src="../../assets/images/ic_bar_back_white.png"/>返回</a>
      <a href="javascript:;" slot="right">分享</a>
    </m-header>
    <m-header title="豆瓣app" fixed>
      <a href="javascript:;" slot="left">< img class="m-icon-img" src="../../assets/images/ic_bar_back_green.png"/>返回</a>
      <a href="javascript:;" slot="right">< img class="m-icon-img margin-right-10" src="../../assets/images/ic_actionbar_search_icon.png"/></a>
      <a href="javascript:;" slot="right">< img class="m-icon-img" src="../../assets/images/ic_chat_green.png"/></a>
    </m-header>
    <m-tabbar v-model="select">
    <m-tabbar-item id="tab1">
      <img src="../assets/images/ic_tab_home_normal.png" alt="" slot="icon-normal"/>
      <img src="../assets/images/ic_tab_home_active.png" alt="" slot="icon-active">
      首页
    </m-tabbar-item>
    <m-tabbar-item id='tab2'>
      <img src="../assets/images/ic_tab_subject_normal.png" alt="" slot="icon-normal">
      <img src="../assets/images/ic_tab_subject_active.png" alt="" slot="icon-active">
      书影音
    </m-tabbar-item>
    <m-tabbar-item id='tab3'>
      <img src="../assets/images/ic_tab_status_normal.png" alt="" slot="icon-normal">
      <img src="../assets/images/ic_tab_status_active.png" alt="" slot="icon-active">
      广播
    </m-tabbar-item>
    <m-tabbar-item id='tab4'>
      <img src="../assets/images/ic_tab_group_normal.png" slot="icon-normal"/>
      <img src="../assets/images/ic_tab_group_active.png" alt="" slot="icon-active">
      小组
    </m-tabbar-item>
    <m-tabbar-item id='tab5'>
      <img src="../assets/images/ic_tab_profile_normal.png" alt="" slot="icon-normal">
      <img src="../assets/images/ic_tab_profile_active.png" alt="" slot="icon-active">
      我的
    </m-tabbar-item>
    </m-tabbar>
  </div>
</template>
<script>
  import mTabbar from '../components/tabbar'
  import mTabbarItem from '../components/tabbar-item'
  export default {
    name: 'Index',
    components: {
      mTabbar,
      mTabbarItem
    },
    data(){
        return{
            select:"tab1"
        }
    }
  }
</script>
