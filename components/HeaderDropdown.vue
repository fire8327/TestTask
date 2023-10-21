<template>
    <div class="relative group">
        <button @click="isDown = !isDown" class="flex items-center gap-4">
            <p>{{ title }}</p>
            <Icon name="ic:outline-keyboard-arrow-down" class="text-xl xl:opacity-0 transition-all duration-500" :class="isDown ? 'xl:opacity-100' : 'xl:group-hover:opacity-100'"/>
        </button>
        <div class="absolute z-50 top-[calc(100%+10px)] shadow-[3px_2px_16px_0px_rgba(0,0,0,0.10)] w-fit flex flex-col rounded-lg transition-all duration-500 bg-white -translate-x-1/2 left-1/2" :class="{'hidden' : !isDown}">
            <NuxtLink @click="isDown = false" v-for="content in contents" :to="content.link" class="transition-all duration-500 hover:bg-gray-200 px-4 py-1.5 first:rounded-t-lg last:rounded-b-lg">{{ content.title }}</NuxtLink>
        </div>
    </div>
</template>

<script setup>
    const isDown = ref(false)
    defineProps({
        title: String,
        contents: Array
    })
</script>