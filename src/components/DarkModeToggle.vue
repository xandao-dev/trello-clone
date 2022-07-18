<script setup lang="ts">
import { useDark, useToggle } from '@vueuse/core'

const isDark = useDark()
const toggleDark = useToggle(isDark)
</script>

<template>
	<button @click="toggleDark()" class="flex items-center justify-center rounded-full p-2 text-white bg-gray-500 hover:bg-orange-500 dark:hover:bg-gray-500 dark:bg-orange-500">
		<span class="material-symbols-rounded" v-text="isDark ? 'light_mode' : 'dark_mode'"></span>
	</button>
</template>
