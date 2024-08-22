<script setup>
    const props = defineProps(['recordingOperation'])
</script>
<template>
    <header class="p-5 mt-5">
        <h1>Calculator VueJS</h1>
        <h3>O resultado da Operação foi: <span>{{ props.recordingOperation }}</span></h3>
    </header>
</template>