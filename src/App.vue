<template>
  <div id="app">
    <h3>Double click on the file node to turn it into a folder</h3>
    <ul>
      <item class="item" :model="treeData"/>
    <ul>
  </div>
</template>

<script>
import Item from './components/Item'

var data = {
  name: 'My Tree',
  children: [
    { name: 'hello' },
    { name: 'wat' },
    {
      name: 'child folder',
      children: [
        {
          name: 'child folder',
          children: [
            { name: 'hello' },
            { name: 'wat' }
          ]
        },
        { name: 'hello' },
        { name: 'wat' },
        {
          name: 'child folder',
          children: [
            { name: 'hello' },
            { name: 'wat' }
          ]
        }
      ]
    }
  ]
}
export default {
  name: 'app',
  data: function () {
    return {
      treeData: data
    }
  },
  components: {
    Item
  }
}
</script>

<style>
.body {
  font-family: Menlo, Consolas, monospace;
  color: #444;
}
.item {
  cursor: pointer;
}
.bold {
  font-weight: bold;
}
ul {
  padding-left: 1em;
  line-height: 1.5em;
  list-style-type: dot;
}
</style>
