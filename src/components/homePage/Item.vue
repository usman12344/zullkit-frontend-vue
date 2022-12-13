<script setup>
import { ref } from 'vue';
import ItemCard from '../ItemCard.vue';

const items = ref([
    {  id: '1', title: 'RoboCrypto App', deskripsi: 'Monile UI Kit', image: 'items-1.jpg'},
    {  id: '2', title: 'Online Doctor Consultation', deskripsi: 'Website UI Kit', image: 'items-2.jpg'},
    {  id: '3', title: 'Banking Crypto', deskripsi: 'Mobile UI Kit', image: 'items-3.jpg'},
])
</script>

<template>
    <div class="container px-4 mx-auto my-16 md:px-12">
        <h2 class="mb-4 text-xl font-medium md:mb-0 md:text-lg">Top Item</h2>
        <div class="flex flex-wrap -mx-1 lg:-mx-4">
            <ItemCard 
            v-for="item in items"
            :key="item.id"
            :title="item.title"
            :deskripsi="item.deskripsi"
            :image="item.image" />
        </div>
    </div>
</template>
