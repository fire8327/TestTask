<template>
    <div class="flex items-center justify-center" :style="`height: calc(100vh - ${header.height}px)`">
        Страница операций
    </div>
</template>

<script setup>    
    const header = useHeader()
</script>