<!-- eslint-disable vue/no-multiple-template-root -->
<template>
  
  <n-card class="banner">
  </n-card>
  <n-card
    title=""

    :segmented="{
      content: true,
      footer: 'soft'
    }"
  >
     <n-grid style="padding-top: 25px;padding-bottom: 25px;" cols="3" item-responsive responsive="screen">
      <n-grid-item v-for="(product, index) in products" style="padding: 20px 20px 20px 20px;">
        <ShopItem :title="product.name" :description="product.description" :img="product.img" :price="product.cost" />
      </n-grid-item>
      <p></p>
    </n-grid>
    <template #footer>
      <n-card class="sub-banner">
      </n-card>
    </template>
    <template #action>
       <n-grid x-gap="12" :cols="3">
        <n-gi>
          <div class="site-map">
            <h3> Site Map</h3>
            <ul>
              <li><a href="#">Shop</a></li>
              <li><a href="#">Cart</a></li>
              <li><a href="#">Contact</a></li>
            </ul>
            <hr>
            <p>
            Location: 
            <br>123 Example Street
            <br>Auckland
            <br>New Zealand
            </p>
          </div>
        </n-gi>
        <n-gi>
          <div>
          </div>
        </n-gi>
        <n-gi>
          <div>
          </div>
        </n-gi>
      </n-grid>
    </template>
  </n-card>
  

  
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
.sub-banner {
  max-width: 100%;
  min-height: 300px;;
  background-color:black;
}
</style>

