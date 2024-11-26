<template>
  <div class="home">
    <div class="slider">
      <div class="title">
        <img src="@/assets/logo.png" alt="" />
        <ModuleName />
      </div>

      <div class="menu-list" v-for="item in menus">
        <div class="menu-item">
          {{ item.title }}
        </div>
      </div>
    </div>
    <div class="content">
      <header></header>
      <main></main>
      <footer></footer>
    </div>
  </div>
</template>

<script setup lang="ts">
import { MenuItem } from '@/models/menu'
import ModuleName from '@fluentui/svg-icons/icons/accessibility_24_regular.svg'

const menus: MenuItem[] = [
  {
    icon: 'icon-home',
    path: '/',
    title: '首页',
  },
  {
    icon: 'icon-home',
    path: '/',
    title: '首页',
  },
]
</script>

<style scoped lang="scss">
.home {
  display: flex;
  flex-direction: row;
  width: 100vw;
  height: 100vh;

  .slider {
    width: 240px;
    background-color: antiquewhite;
    padding: 24px;

    .title {
      width: 72px;
    }
  }

  .content {
    flex-grow: 1;
  }
}
</style>
