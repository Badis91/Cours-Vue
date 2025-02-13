<template>
    <article>
        <label :for="data.id"></label>
        <input 
        :type="data.type ? data.type : 'text'" 
        :placeholder="data.text"  
        />

    </article>
</template>

<script setup lang="ts">
import type ButtonInterface from '../interfaces/ButtonInterface';


interface FieldComponentProperties {
    data: ButtonInterface
}

defineProps<FieldComponentProperties>()

</script>