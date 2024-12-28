<script setup lang="ts">
// import Item interface
import type { ItemInterface } from '../../models/items/Item.interface'

// items property with a blank array
defineProps<{ items: ItemInterface[] }>()

// define emits for custom events
const emit = defineEmits<{
    (e: 'selectItem', id: number): any
}>()

// item click handler
const handleClick = (item: ItemInterface) => {
    emit('selectItem', item.id)
}
</script>

<template>
    <div>
        <h3>Items:</h3>
        <ul>
            <li v-for="(item, index) in items"
                :key="item.id"
                @click="handleClick(item)">
                {{ item.name }} [{{ item.selected }}]
            </li>
        </ul>
    </div>
</template>