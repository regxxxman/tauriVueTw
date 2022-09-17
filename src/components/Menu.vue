<script setup>
import { appWindow } from '@tauri-apps/api/window'
</script>

<template>
  <div>
    <div
      data-tauri-drag-region
      class="w-full h-6 bg-slate-500 opacity-70 flex justify-end"
    >
      <!-- <div class="justify-center">title</div> -->
      <div
        @click="appWindow.minimize()"
        class="bg-green-500 hover:opacity-50 h-full w-6 rounded-lg mx-1"
      ></div>

      <div
        @click="appWindow.toggleMaximize()"
        class="bg-yellow-500 hover:opacity-50 h-full w-6 rounded-lg mx-1"
      ></div>
      <div
        @click="appWindow.close()"
        class="bg-red-500 hover:opacity-50 h-full w-6 rounded-lg mx-1 mr-2"
      ></div>
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

<style></style>
