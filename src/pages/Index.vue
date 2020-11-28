<template>
  <q-page>
    <svg id ="canvas" wigth="400" height="300">
      <node v-for = "n in nodes" :key ="n.t"  :x = "n.x" :y = "n.y" :t = "n.t" :v = "n.v"></node>

      <edge v-for = "e in edges" :key ="e.t"  :x = "e.x" :y = "e.y" :t = "e.t" :v = "e.v"></edge>
    </svg>
    <br/>
    <table>
      <tr v-for = "n in nodes" :key="n.t">
        <td><input v-model="n.t"/></td>
        <td><input type="number" v-model="n.v"/></td>
        <td><input type="number" v-model="n.x"/></td>
        <td><input type="number" v-model="n.y"/></td>
      </tr>
    </table>
  </q-page>
</template>

<script>

import Node from 'components/Node.vue'
import Edge from 'components/Edge.vue'

export default {
  name: 'PageIndex',
  components: { Node, Edge },
  data () {
    return {
      nodes: [{
        x: 100,
        y: 100,
        t: 'TEST',
        v: 60
      },
      {
        x: 50,
        y: 200,
        t: 'TEST2',
        v: 80
      }],
      edges: []
    }
  }
}
</script>
