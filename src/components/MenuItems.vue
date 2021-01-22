<template>
  <div class="menu__item">
    <div class="menu__item--icon" :class="item.icon_class"></div>
    <div class="menu__item--text">
        {{ item.name }}
    </div>
  </div>
</template>

<script>
export default {
  name: 'Menu-item',
  data() {
    return {

    }
  },
  props: {
    item: Object,
  },
}
</script>

<style>

</style>
