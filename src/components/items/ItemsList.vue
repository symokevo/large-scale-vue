<script setup lang="ts">
// items property with a blank array
defineProps<{ items: any[] }>()
</script>

<template>
    <div>
        <h3>Items:</h3>
        <ul>
            <li v-for="(item, index) in items"
                :key="item.id">
                {{ item.name }}
            </li>
        </ul>
    </div>
</template>