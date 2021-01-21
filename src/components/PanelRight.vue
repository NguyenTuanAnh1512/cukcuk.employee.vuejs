<template>
  <div class="panel-right">
    <!--Header-->
    <Header />
    <!--Content-->
    <Content></Content>
  </div>
</template>

<script>
import Header from './Header.vue'
import Content from './Content.vue'

export default {
  name: 'panel-right',
  components: {
    Header,
    Content,
  },
  data() {
    return {

    }
  },
}
</script>

<style>
.panel-right {
    width: calc(100% - 200px);
    height: 100vh;
    position: absolute;
    top: 0;
    left: 200px;
}
</style>
