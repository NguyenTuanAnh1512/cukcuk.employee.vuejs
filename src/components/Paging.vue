<template>
  <div class="paging">
    <p>Hiển thị <b>1-10/1000</b> khách hàng</p>

    <div class="control_page">
        <div class="icon_page icon_firstpage"></div>
        <div class="icon_page icon_prevpage"></div>

        <div class="page" style="background-color: #00a86f">1</div>
        <div class="page">2</div>
        <div class="page">3</div>
        <div class="page">4</div>

        <div class="icon_page icon_nextpage"></div>
        <div class="icon_page icon_lastpage"></div>
    </div>

    <p><b>10</b> khách hàng/trang</p>
  </div>
</template>

<script>
export default {
  name: 'paging',
  data() {
    return {

    }
  },
}
</script>

<style>

</style>
