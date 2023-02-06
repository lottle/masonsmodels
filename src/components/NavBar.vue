<template>
    <n-grid cols="4" item-responsive responsive="screen">
        <n-grid-item span="0 m:1 l:2">
            <div>
                <h2>Masons Models</h2>
            </div>
        </n-grid-item>
        <n-grid-item>
            <div>
                <n-menu v-model:value="activeKey" mode="horizontal" :options="menuOptions" />
            </div>
        </n-grid-item>
    </n-grid>
    
  </template>
  
  <script lang="ts">
  import { defineComponent, h, ref, Component } from 'vue'
  import { NIcon, NGrid, NGridItem } from 'naive-ui'
  import type { MenuOption } from 'naive-ui'
  import {
    HomeOutline as HomeIcon,
    BasketOutline as ShopIcon,
    Pencil as ContactIcon
  } from '@vicons/ionicons5'
  
  function renderIcon (icon: Component) {
    return () => h(NIcon, null, { default: () => h(icon) })
  }
  
  const menuOptions: MenuOption[] = [
    {
      label: 'Home',
      key: 'home',
      icon: renderIcon(HomeIcon),
    },
    {
      label: 'Shop',
      key: 'shop',
      icon: renderIcon(ShopIcon)
    },
    {
      label: 'Contact',
      key: 'contact',
      icon: renderIcon(ContactIcon)
    }
  ]
  
  export default defineComponent({
    setup () {
      return {
        activeKey: ref<string | null>(null),
        menuOptions
      }
    }
  })
  </script>
  