<template>
  <div class="header">
    <div class="restaurant">
        <span>Nhà hàng Biển Đông</span>
        <div class="icon_dropdown"></div>
    </div>
    <div class="name__user">
        <div class="icon_avatar"></div>
        <span>Nguyễn Tuấn Anh</span>
        <div class="icon_option"></div>
    </div>
  </div>
</template>

<script>
export default {
 name: 'Header',
 data() {
   return {

   }
 },
}
</script>

<style>
  .header {
    height: 60px;
    width: 100%;
    display: flex;
    align-items: center;
    border-bottom: 1px solid #bfbfbf;
}

    .header .restaurant {
        height: 30px;
        display: flex;
        align-items: center;
        margin-left: 40px;
        height: 50px;
        padding-left: 20px;
        padding-right: 20px;
        border-radius: 4px;
        cursor: pointer;
    }

        .header .restaurant:hover {
            background-color: #e3e3e3;
        }

        .header .restaurant .icon_dropdown {
            background-image: url('/content/icon/dropdown.png');
            background-size: cover;
            width: 12px;
            height: 12px;
            margin-left: 10px;
            cursor: pointer;
        }

    .header .name__user {
        height: 30px;
        display: flex;
        align-items: center;
        position: absolute;
        right: 10px;
        height: 50px;
        padding-left: 20px;
        padding-right: 20px;
        border-radius: 4px;
        cursor: pointer;
    }

        .header .name__user:hover {
            background-color: #e3e3e3;
        }

        .header .name__user .icon_avatar {
            background-image: url('/content/icon/avatar-default.png');
            width: 30px;
            height: 30px;
            background-size: contain;
            margin-right: 8px;
        }

        .header .name__user .icon_option {
            background-image: url('/content/icon/option.png');
            width: 15px;
            height: 15px;
            margin-left: 8px;
            background-size: cover;
            cursor: pointer;
        }
</style>
