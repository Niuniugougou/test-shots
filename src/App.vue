<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import { ipcRenderer } from 'electron';
const test = () => {
  ipcRenderer.send('startCapture')
}
</script>

<template>
  <HelloWorld msg="Electron + Vite + Vue" />
  <button @click="test">截图</button>
</template>

<style>
.flex-center {
  display: flex;
  align-items: center;
  justify-content: center;
}

.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}

.logo.electron:hover {
  filter: drop-shadow(0 0 2em #9FEAF9);
}

.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}

.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
