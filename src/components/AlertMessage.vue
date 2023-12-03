<template>
    <v-alert :type="typeValue" closable="true" close-label="Close Alert" variant="tonal">
        <slot name="title"></slot>
        <slot></slot>
    </v-alert>
</template>

<script setup>
defineProps({
    typeValue: {
        type: String,
        required: true
    }
})
</script>