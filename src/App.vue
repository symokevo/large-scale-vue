<script setup lang="ts">
// import ItemsList component
import ItemsList from './components/items/ItemsList.vue'
// mock some data
const items: any[] = [{
  id: 1,
  name: 'Item 1'
}, {
  id: 2,
  name: 'Item 2'
}, {
  id: 3,
  name: 'Item 3'
}]
</script>

<template>
  <div class="home">
    <ItemsList :items="items"/>
  </div>
</template>

<style scoped>

</style>
