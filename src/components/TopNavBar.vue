<script setup>
import { ref, defineEmits } from 'vue'

const emits = defineEmits(['navigate'])
const menuItems = ref(['Home', 'About', 'Projects', 'Gallery', 'Contact']);

const handleClick = (item) => {
  emits('navigate', item.toLowerCase());
}
</script>

<template>
    <nav class="py-12 w-full transition-all ease-in-out duration-500 bg-transparent">
        <div class="container mx-auto px-4">
            <a class="float-left text-2xl font-bold text-white">Khai Loong's Curriculum Vitae</a>
            <div class="flex justify-end">
                <ul class="flex space-x-8">
                    <li v-for="item in menuItems" :key="item">
                        <a @click.prevent="handleClick(item)" class="cursor-pointer text-white text-xl uppercase font-semibold transition-all duration-500 hover:text-blue-500">{{ item }}</a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</template>
