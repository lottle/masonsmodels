<template>
    <n-card v-bind:title="title">
      <template #header-extra>
        {{price}}
      </template>
      <template #cover>
        <img v-bind:src="`/assets/img/${img}`" />
      </template>
      

      {{ description }} 
      <n-space>
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
.n-space {
  padding-top: 25px;
}
</style>