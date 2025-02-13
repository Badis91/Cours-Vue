<template>

<button :id="data.id" :type="data.type ?? 'text'">Reinitialiser</button>

</template>

<script setup lang="ts">

interface ButtonComponentProperties {
    data: {
        id: string,
        type: 'button' | 'submit' | 'reset',
    }
}

defineProps<ButtonComponentProperties>()

</script>