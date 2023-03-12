<!-- eslint-disable vue/no-multiple-template-root -->
<template>
  <n-card class="banner">
  </n-card>
  <n-grid style="padding-top: 20px;" cols="3" item-responsive responsive="screen">
    <n-grid-item v-for="(product, index) in products" style="padding: 20px 20px 20px 20px;">
      <ShopItem :title="product.name" :description="product.description" :img="product.img" :price="product.cost" />
    </n-grid-item>
    <p></p>
  </n-grid>
</template>

<script lang="ts">
  import { defineComponent, h, ref, Component } from 'vue';
  import { NIcon, NGrid, NGridItem } from 'naive-ui';
  import ShopItem from './ShopItem.vue';
  import productData from '../assets/data/products.json';

  const MAX_HOME_ITEMS = 6;

  export default defineComponent({
    components:{
      ShopItem
    },
    data() {
      return {
        products: productData
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

