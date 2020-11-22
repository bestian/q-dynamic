<template>
  <g>
    <rect :x = "x" :y = "y" width="100" height="62" style="fill:rgb(0,0,255);stroke-width:3;stroke:rgb(0,0,0)">
      <text> {{ t }}</text>
      <text> {{ v }}</text>
    </rect>
  </g>
</template>

<script>
export default {
  name: 'Node',
  props: ['x', 'y', 't', 'v']
}
</script>
