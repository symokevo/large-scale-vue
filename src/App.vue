<script setup lang="ts">
// import Item interface
import type { ItemInterface } from '../../models/items/Item.interface'

// import ItemsList component
import ItemsList from './components/items/ItemsList.vue'
// mock some data
const items: ItemInterface[] = [{
  id: 1,
  name: 'Item 1',
  selected: false
}, {
  id: 2,
  name: 'Item 2',
  selected: false
}, {
  id: 3,
  name: 'Item 3',
  selected: false
}]
</script>

<template>
  <div class="home">
    <ItemsList :items="items"/>
  </div>
</template>

<style scoped>

</style>
