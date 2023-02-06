<template>
  <NavBar/>
  <HomePage/>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import HomePage from './components/HomePage.vue';
import NavBar from './components/NavBar.vue';

export default defineComponent({
  components:{
    NavBar,
    HomePage
  }
})

</script>

