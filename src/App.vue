<script setup lang="ts">
// import vue reactive
import { reactive } from 'vue';
// import Item interface
import type { ItemInterface } from '../../models/items/Item.interface'

// import ItemsList component
import ItemsList from './components/items/ItemsList.vue'
// mock some data
const items= reactive([
  {
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
}]);

// selectItem handler
const onSelectItem = (id: number) => {
  // retrieve the item from local data
  const item = items.find(o => o.id === id);

  // Check
  if(!item) {
    console.warn(`onSelectItem: could not find item with id: ${ id }`)
    return
  }

  // Update the item property
  item.selected = !item.selected;
  console.log('onSelecteItem', item.id, item.selected)
}
</script>

<template>
  <div class="home">
    <ItemsList :items="items" @selectItem="onSelectItem"/>
  </div>
</template>

<style scoped>

</style>
