<template>
  <div>
    <button @click.ctrl="ctrlClicked">Ctrl + Click Me</button>
    <button @click.ctrl.shift="comboClicked">Ctrl + Shift + Click Me</button>
    <input @keyup.alt.c="onAltC" placeholder="Press Alt + C">
  </div>
</template>

<script>
export default {
  methods: {
    ctrlClicked() {
      alert("Control + Click detectado!");
    },
    comboClicked() {
      alert("Control + Shift + Click detectado!");
    },
    onAltC() {
      alert("Alt + C detectado!");
    }
  }
}
</script>