<template>
  <div class="mb-13">
    <header>
      <h1 class="text-5xl">Welcome</h1>
    </header>
    <section class="mt-10">
      <p>Draw a random number</p>
      <button
        class="m-3 text-sm btn outline-none font-bold tracking-widest"
        @click="drawRandomNum"
      >
        DRAW
      </button>
      <p>{{ randomNum }}</p>
    </section>
  </div>
</template>

<script setup lang="ts">
let randomNum = ref(0)

const drawRandomNum = () => (randomNum.value = Math.round(Math.random() * 100))
</script>


<style scoped>
.outline-none {
  outline: none;
}
</style>
