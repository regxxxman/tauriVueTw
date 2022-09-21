<script setup>
import { appWindow } from '@tauri-apps/api/window'
</script>

<template>
  <div>
    <div class="flex bg-stone-800 bg-opacity-90">
      <div
        data-tauri-drag-region
        class="w-full h-6 flex justify-end text-white"
      >
        <button
          v-for="item in items"
          class="hover:bg-opacity-50 m-0.5 h-5 w-5 rounded-full mx-1"
          :class="{
            'bg-opacity-50': !item.active,
            'bg-green-500': item.massage == 'min',
            'bg-yellow-500': item.massage == 'max',
            'bg-red-500': item.massage == 'close',
          }"
          @click="MenuItemEvent(item)"
        ></button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    MenuItemEvent(item) {
      if (item.massage == 'min' && item.active) {
        appWindow.minimize()
      } else if (item.massage == 'max' && item.active) {
        appWindow.maximize()
      } else if (item.massage == 'close' && item.active) {
        appWindow.close()
      } else {
      }
    },
    classExtraction(item) {
      return item.categories.map((cat) => cat.name)
    },
  },
  data() {
    return {
      items: [
        { massage: 'min', active: true },
        { massage: 'max', active: true },
        { massage: 'close', active: true },
      ],
    }
  },
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Material+Symbols+Rounded:opsz,wght,FILL,GRAD@20..48,100..700,0..1,-50..200');
.material-symbols-rounded {
  font-variation-settings: 'FILL' 0, 'wght' 700, 'GRAD' 0, 'opsz' 48;
}
</style>
