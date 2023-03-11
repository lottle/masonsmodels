<!-- eslint-disable vue/no-multiple-template-root -->
<template>
  <n-card class="banner">
  </n-card>
  <n-grid style="padding-top: 20px;" cols="3" item-responsive responsive="screen">
    <n-grid-item v-for="item in items" style="padding: 20px 20px 20px 20px;">
      <ShopItem/>
    </n-grid-item>
  </n-grid>
</template>

<script lang="ts">
  import { defineComponent, h, ref, Component } from 'vue'
  import { NIcon, NGrid, NGridItem } from 'naive-ui'
  import ShopItem from './ShopItem.vue';
  import products from '../assets/data/products.json';

  const MAX_HOME_ITEMS = 6;

  export default defineComponent({
  components:{
    ShopItem
  },
  data() {
    return {
      items: products
    }
  }
})
</script>

<style scoped>
.banner {
  max-width: 100%;
  min-height: 600px;;
  background-color:black;
}
</style>

