<script setup lang="ts">
import { ref } from 'vue'

defineProps<{ msg: string }>()

const a = ref(0)
const b = ref(0)
const total = ref(0)
</script>

<template>
  <h1 class="text-3xl font-bold underline hover:text-sky-400">
    {{ msg }}
  </h1>

  <p>
    <a href="https://vitejs.dev/guide/features.html" target="_blank">
      Vite Docs
    </a>
    |
    <a href="https://v3.vuejs.org/" target="_blank">Vue 3 Docs</a>
  </p>

  <input v-model="a" type="number" />
  <input v-model="b" type="number" />
  <button type="button" @click="total = a + b">result is: {{ total }}</button>
  <p>
    Edit
    <code>components/HelloWorld.vue</code> to test hot module replacement.
  </p>
</template>

<style scoped></style>
