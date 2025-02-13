<template>
<form class="login-form">
    
    <section>
        <FieldComponent v-for = "(fields,index) in data.fields" 
        :key="index"
        :data="fields" />
    </section>
    <section id="actions">
        <ButtonComponent v-for = "(buttons,index) in data.buttons" 
        :key="index"
        :data="buttons" />
    </section>
</form>
</template>


<script setup lang="ts">
import ButtonComponent from './ButtonComponent.vue';
import FieldComponent from './FieldComponent.vue';


interface FormComponentProperties {
    data:{
        fields: {
            id: string,
            type: string,
            placeholder: string
        }[],
        buttons: {
            id: string,
            type: 'button' | 'submit' | 'reset',
            text: string
        }[]
    }
}

defineProps<FormComponentProperties>()


</script>
