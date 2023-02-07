<script setup lang="ts">
import { useSlots,PropType } from 'vue';
type Value = string | number | boolean
const props = defineProps({
    modelValue: {
        type: [String, Number, Boolean] as PropType<Value>,
        default: ''
    },
})
const slots = useSlots()

</script>
<template>
    <div>
        <slot></slot>
    </div>
</template>