<script setup lang="ts">
import { ref } from "vue";
import { useCounterStore } from "../stores/counter";

defineProps<{ msg: string }>();

//const count = ref(0)

const counterStore = useCounterStore();
</script>

<template>
  <h1>{{ msg }}</h1>

  <div class="card">
    <div>count from store {{ counterStore.count }}</div>
    <button type="button" @click="counterStore.increment">+</button>
    <button type="button" @click="counterStore.decrement">-</button>
    <p>
      Edit
      <code>components/HelloWorld.vue</code> to test HMR
    </p>
  </div>

  <p>
    Check out
    <a href="https://vuejs.org/guide/quick-start.html#local" target="_blank"
      >create-vue</a
    >, the official Vue + Vite starter HelloWorld
  </p>
  <p>
    Learn more about IDE Support for Vue in the associated Vite + Vue
    <a href="https://vitejs.dev/guide/features.html#ide-support" target="_blank"
      >Vite Docs</a
    >
    and the
    <a
      href="https://vuejs.org/guide/scaling-up/tooling.html#ide-support"
      target="_blank"
      >Vue Docs</a
    >. You can also check out the
    <a
      href="https://vuejs.org/guide/scaling-up/tooling.html#ide-support"
      target="_blank"
      >Vue Docs Scaling up Guide</a
    >.
  </p>
  <p>
    Check out
    <a href="https://vuejs.org/guide/quick-start.html#local" target="_blank"
      >create-vue</a
    >, the official Vue + Vite starter HelloWorld
  </p>
  <p>
    Learn more about IDE Support for Vue in the associated Vite + Vue
    <a
      href="https://vuejs.org/guide/scaling-up/tooling.html#ide-support"
      target="_blank"
      >Vue Docs Scaling up Guide</a
    >.
  </p>
  <p class="read-the-docs">Click on the Vite and Vue logos to learn more</p>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
