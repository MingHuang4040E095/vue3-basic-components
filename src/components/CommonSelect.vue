<script setup lang="ts">
import { PropType } from 'vue';


type Value = string | number | boolean

const props = defineProps({
    modelValue: {
        type: [String,Number] as PropType<Value>,
        default: ''
    },

})

</script>

<template>
    <div>
        <input type="text" />
        <Teleport to="body">
            <ul>
                <slot></slot>
            </ul>
        </Teleport>
    </div>
</template>