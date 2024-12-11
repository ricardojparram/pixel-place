<template><canvas id="canvas" width="4000" height="2000"></canvas></template>
<

<script setup>
import { onMounted } from 'vue'
onMounted(() => {
  console.log('hola')
  const canvas = document.getElementById('canvas')
  console.log(canvas)
  const c2d = canvas.getContext('2d')
  c2d.strokeStyle = '#cbd5e1'

  //   c2d.fillStyle = 'red'
  //   c2d.fillRect(50, 0, 50, 50)

  for (var i = 0; i < canvas.width; i += 20) {
    c2d.beginPath()
    c2d.moveTo(i, 0)
    c2d.lineTo(i, canvas.height)
    c2d.stroke()
  }
  for (var i = 0; i < canvas.height; i += 20) {
    c2d.beginPath()
    c2d.moveTo(0, i)
    c2d.lineTo(canvas.width, i)
    c2d.stroke()
  }
})
</script>
