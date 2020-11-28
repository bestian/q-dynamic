<template>
  <g>
    <rect :x = "x" :y = "y" width="100" height="62" style="fill:rgb(0,0,255);stroke-width:3;stroke:rgb(0,0,0)">
    </rect>
    <text :x = "x + 20" :y = "y + 20" >{{ t }}</text>
    <text :x = "x + 20" :y = "y + 50" >{{ v }}</text>
  </g>
</template>

<script>
export default {
  name: 'Node',
  props: ['x', 'y', 't', 'v']
}
</script>

<style type="text/css" scoped="">
    text {
        position: relative;
        z-index: 9;
    }
</style>
