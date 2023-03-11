<!-- eslint-disable vue/no-multiple-template-root -->
<template>
  <n-card class="banner">
  </n-card>
  <n-grid style="padding-top: 20px;" cols="3" item-responsive responsive="screen">
    <n-grid-item style="padding: 20px 20px 20px 20px;">
      <ShopItem/>
    </n-grid-item>
  </n-grid>
</template>

<script lang="ts">
  import { defineComponent, h, ref, Component } from 'vue'
  import { NIcon, NGrid, NGridItem } from 'naive-ui'
  import ShopItem from './ShopItem.vue';

  export default defineComponent({
  components:{
    ShopItem
  }
})
</script>

<style scoped>
.banner {
  max-width: 100%;
  min-height: 400px;;
  background-color:black;
}
</style>

