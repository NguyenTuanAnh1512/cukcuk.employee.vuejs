<template>
  <div class="left-menu">
        <!--Logo-->
        <div class="logo">
            <div class="expend-icon"></div>
            <div class="logo-page"></div>
        </div>

        <!--menu-->
        <div class="menu">
          <Menu-item
            v-for="(item, index) in menu_items" :key="index"
            v-bind:item = item
          ></Menu-item>
        </div>
    </div>
</template>

<script>
import MenuItem from './MenuItems';

export default {
  components: { MenuItem },
  name: "left-menu",
  data() {
    return {
      menu_items: [{
        name: 'Tổng quan',
        icon_class: 'icon_dashboard',
        },
        {
          name: 'Báo cáo',
          icon_class: 'icon_report',
        },
        {
          name: 'Mua hàng',
          icon_class: 'icon_dashboard',
        },
        {
          name: 'Danh mục khách hàng',
          icon_class: 'icon_dic-employee',
        },
        {
          name: 'Thiết lập hệ thống',
          icon_class: 'icon_setting',
      }]
    }
  },
}
</script>


<style>
.menu {

}

.menu .menu__item {
display: flex;
align-items: center;
width: 100%;
height: 44px;
}

.menu .menu__item:hover {
    background-color: #e3e3e3;
    cursor: pointer;
}

.menu .menu__item .menu__item--icon {
    width: 20px;
    height: 20px;
    background-size: cover;
    margin-left: 16px;
}

.menu .menu__item .menu__item--text {
    margin-left: 4px;
}
  .left-menu {
      width: 200px;
      height: 100vh;
      border-right: 1px solid #bfbfbf;
      background-color: #ffffff;
  }

  .left-menu .logo {
      height: 60px;
      width: 100%;
      display: flex;
      align-items: center; /*căn giữa khi dùng display: flex;*/
      /*background-color: red;*/
  }

  .left-menu .logo .expend-icon {
      width: 30px;
      height: 30px;
      background-image: url(/content/img/toggle.png);
      background-size: cover;
      background-position: center;
      margin-left: 16px;
      background-repeat: no-repeat;
  }

  .left-menu .logo .logo-page {
      width: 100%;
      height: 34px;
      background-image: url(/content/img/cukcuk-logo.png);
      background-size: contain;
      background-repeat: no-repeat;
      margin-left: 10px;
  }
</style>
