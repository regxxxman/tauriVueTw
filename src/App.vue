<script setup>
import Menu from './components/Menu.vue'
// import MenuWindow from './components/MenuWindow.vue'
</script>

<template>
  <Menu />
  <div class="absolute h-full w-full">
    <div
      class="text-white p-5 w-full relative overflow-y-auto max-h-full scrollbar-thin scrollbar-thumb-slate-700 scrollbar-track-slate-500 scrollbar-thumb-rounded-full scrollbar-track-rounded-full"
    >
      <h1 class="text-center">Добро пожаловать в программу</h1>
      <img
        class="m-auto h-full w-full rounded-lg"
        src="https://sun1.beltelecom-by-minsk.userapi.com/impg/QrP_K7H19u0a3S353Z4PM80b6sOHlDfhvsh8MA/nkpxtTYaLBA.jpg?size=773x1080&quality=96&sign=d3b24651555c260806b1d5f66529501d&type=album"
        alt=""
      />

      <div class="h-10"></div>
    </div>
  </div>
  <!-- <MenuWindow /> -->
</template>

<style></style>
