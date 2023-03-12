<template>
    <n-card v-bind:title="title">
      <template #cover>
        <img v-bind:src="`../assets/products/${img}`">
      </template>

      {{ description }} 
      <n-space >
        <n-button>View</n-button>
        <n-button type="primary">
          Add to Cart
        </n-button>
        </n-space>
    </n-card>
  </template>

<script>
export default {
  
  props: {
    title: String,
    description: String,
    img: String,
    price: String
  }
}
</script>  

<style scoped>
.n-card {
  max-width: 300px;
}
.n-space {
  padding-top: 10px;
   text-align: center;
}
</style>