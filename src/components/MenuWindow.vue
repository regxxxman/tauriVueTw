<script setup>
import { appWindow } from '@tauri-apps/api/window'

</script>

<template>
  <div data-tauri-drag-region class="titlebar">
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
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Material+Symbols+Rounded:opsz,wght,FILL,GRAD@48,400,0,0');

.material-symbols-rounded {
  font-variation-settings: 'FILL' 0, 'wght' 400, 'GRAD' 0, 'opsz' 48;
}

#titlebar-minimize {
  color: green;
}

#titlebar-maximize {
  color: yellow;
}

#titlebar-close {
  color: red;
}

.titlebar {
  height: 30px;
  /* background: #329da388; */
  background: rgba(0, 0, 0, 0.178);
  user-select: none;
  display: flex;
  justify-content: flex-end;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
}
.titlebar-button {
  display: inline-flex;
  justify-content: center;
  align-items: center;
  width: 30px;
  height: 30px;
}
.titlebar-button:hover {
  background: #5bbec393;
}
</style>
