<script setup>
import MenuWindow from './components/MenuWindow.vue'
import MenuOptions from './components/MenuOptions.vue'
// import MenuWindow from './components/MenuWindow.vue'
</script>

<template>
  <MenuWindow />

  <!-- <ul
    class="z-50 absolute menu w-56 p-2 rounded-box bg-slate-500 bg-opacity-50 backdrop-blur-sm"
  >
    <li><a>Item 1</a></li>
    <li><a>Item 2</a></li>
    <li><a>Item 3</a></li>
  </ul> -->
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
      <button class="btn glass">Glass button</button>
      <input type="text" placeholder="Type here" class="input w-full" />
      <select class="my-5 select w-full">
        <option disabled selected>Pick your favorite Simpson</option>
        <option>Homer</option>
        <option>Marge</option>
        <option>Bart</option>
        <option>Lisa</option>
        <option>Maggie</option>
      </select>
      <div class="h-10"></div>
    </div>
  </div>
  <MenuOptions />

  <!-- <div
    class="bg-slate-500 bg-opacity-50 backdrop-blur-sm absolute h-full w-1/3"
  >
    <ul class="z-50 text-center w-full absolute menu p-2 rounded-box">
      <li><a>Item 1</a></li>
      <li><a>Item 2</a></li>
      <li><a>Item 3</a></li>
    </ul>
  </div> -->
  <!-- <MenuWindow /> -->
</template>

<style></style>
