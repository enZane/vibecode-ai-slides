<!-- #context7 FallingCard component: customizable falling card with v-motion props -->
<script setup lang="ts">
import { defineProps } from 'vue'

const { enter, initial } = defineProps<{
    name: string
    iconBg: string
    textColor: string
    initial: Record<string, any>
    enter: Record<string, any>
}>()

const defaultInitial = {
    y: -120,
    opacity: 0,
    
}
const defaultEnter = {
    y: 0,
    opacity: 1,
    transition: { duration: 2000, delay: 200 }
}

const resolvedInitial = { ...defaultInitial, ...initial }
const resolvedEnter = { ...defaultEnter, ...enter }
</script>

<template>
    <div v-motion v-bind:initial="resolvedInitial" v-bind:enter="resolvedEnter"
        class="absolute flex items-center gap-4 p-3 rounded-lg shadow-lg bg-gray-800/90 backdrop-blur-sm border border-gray-700">
        <!-- SVG placeholder icon -->
        <div :class="`w-10 h-10 ${iconBg} rounded-full`"></div>
        <span :class="`text-2xl font-bold ${textColor}`">{{ name }}</span>
    </div>
</template>
