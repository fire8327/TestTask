<template>
    <div class="flex items-center justify-center" :style="`height: calc(100vh - ${header.height}px)`">
        Страница входа
    </div>
</template>

<script setup>    
    const header = useHeader()
</script>