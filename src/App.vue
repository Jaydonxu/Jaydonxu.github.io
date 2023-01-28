<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import { useStore } from './pinia/user'

const counter = useStore()

function addCount() {
  console.log('xxx')
  counter.count++
  // 带有自动补全 ✨
  // counter.$patch({ count: counter.count + 1 })
  // 或者使用 action 代替
  // counter.increment()
}
</script>

<template>
  <div>
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
    <button @click="addCount">确定</button>
    <div>{{ counter.count }}</div>
  </div>
  <HelloWorld msg="Vite + Vue" />
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
