<script setup>
import { appWindow } from '@tauri-apps/api/window'
</script>

<template>
  <div>
    <div class="flex bg-slate-500">
      <!-- <button @click="Menu()" class="ml-2 text-white material-symbols-rounded">
        menu
      </button> -->

      <div
        data-tauri-drag-region
        class="w-full h-6 flex justify-end text-white"
      >
        <!-- <div class="justify-center">title</div> -->
        <button
          @click="appWindow.minimize()"
          class="bg-green-500 hover:bg-opacity-50 h-full w-6 rounded-lg mx-1"
        >
          <span class="material-symbols-rounded opacity-0 hover:opacity-100">
            expand_more
          </span>
        </button>

        <button
          @click="appWindow.toggleMaximize()"
          class="bg-yellow-500 hover:bg-opacity-50 h-full w-6 rounded-lg mx-1"
        >
          <span class="material-symbols-rounded opacity-0 hover:opacity-100">
            open_in_full
          </span>
        </button>
        <button
          @click="appWindow.close()"
          class="bg-red-500 hover:bg-opacity-50 h-full w-6 rounded-lg mx-1 mr-2"
        >
          <span class="material-symbols-rounded opacity-0 hover:opacity-100">
            close
          </span>
        </button>
      </div>
    </div>
  </div>
  <!-- <div data-tauri-drag-region class="titlebar">
    <div
      @click="appWindow.minimize()"
      class="titlebar-button"
      id="titlebar-minimize"
    >
      <span class="material-symbols-rounded"> expand_more </span>
    </div>

    <div
      @click="appWindow.toggleMaximize()"
      class="titlebar-button"
      id="titlebar-maximize"
    >
      <span class="material-symbols-rounded"> open_in_full </span>
    </div>

    <div @click="appWindow.close()" class="titlebar-button" id="titlebar-close">
      <span class="material-symbols-rounded"> close </span>
    </div>
  </div> -->
</template>

<script>
export default {
  methods: {
    Menu() {
      alert('menu')
    },
  },
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Material+Symbols+Rounded:opsz,wght,FILL,GRAD@20..48,100..700,0..1,-50..200');
.material-symbols-rounded {
  font-variation-settings: 'FILL' 0, 'wght' 700, 'GRAD' 0, 'opsz' 48;
}
</style>
