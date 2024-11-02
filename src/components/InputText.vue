<script setup lang="ts">
import { defineProps, defineEmits, ref } from 'vue'

const props = defineProps({
    title: { type: String, required: true },
    inputValue: {type: String, required: true}
})

const emit = defineEmits(['update:inputValue'])

const localInputValue = ref(props.inputValue)

const updateValue = (value: string) => {
    localInputValue.value = value
    emit('update:inputValue', value)
}

</script>

<template>
    <label>{{props.title}}</label>
    <input v-model="props.inputValue" />
</template>

<style scoped>

</style>