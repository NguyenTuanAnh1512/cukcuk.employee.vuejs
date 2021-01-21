<template>
  <div class="left-menu">
        <!--Logo-->
        <div class="logo">
            <div class="expend-icon"></div>
            <div class="logo-page"></div>
        </div>

        <!--menu-->
        <div class="menu">
            <div class="menu__item">
                <div class="menu__item--icon icon_dashboard"></div>
                <div class="menu__item--text">
                    Tổng quan
                </div>
            </div>
            <div class="menu__item">
                <div class="menu__item--icon icon_report"></div>
                <div class="menu__item--text">
                    Báo cáo
                </div>
            </div>
            <div class="menu__item">
                <div class="menu__item--icon icon_dashboard"></div>
                <div class="menu__item--text">
                    Mua hàng
                </div>
            </div>
            <div class="menu__item">
                <div class="menu__item--icon icon_dic-employee"></div>
                <div class="menu__item--text">
                    Danh mục khách hàng
                </div>
            </div>
            <div class="menu__item">
                <div class="menu__item--icon icon_dic-employee"></div>
                <div class="menu__item--text">
                    Danh mục khách hàng
                </div>
            </div>
            <div class="menu__item">
                <div class="menu__item--icon icon_setting"></div>
                <div class="menu__item--text">
                    Thiết lập hệ thống
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: "left-menu",
  data() {
    return {

    }
  },
}
</script>

<style>
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
