<script setup lang="ts">
import {computed} from 'vue'
interface Props {
    modelValue: string | number | boolean
    value: string | number | boolean
    label: string
    size?: 'large' | 'small' | 'default'
}
// 因為用ts所以要用withDefaults來設定預設值
const props = withDefaults(defineProps<Props>(),{
    modelValue: '',
    value: '',
    label: '標籤',
    size: 'default'
})

// const props = defineProps({
//     modelValue: {
//         type: 
//     }
// })

const emit = defineEmits(['update:modelValue'])
const modelValue = computed({
    get(){
        return props.modelValue
    },
    set(value){
        console.log(value)
        emit('update:modelValue', value)
    }
})

// const foo = <T, > (x: T) :T=> {
//     return x*4
// }

// const add = <T>(num:T) : T => {
//     return num
// }
// console.log(add<number>(4))
// console.log(add<string>('4'))
</script>
<template>
    <div>
        <input v-model="modelValue" type="radio" :value="props.value"/>
        <span>{{ props.label }}</span>
    </div>
</template>
<style lang="scss" scoped>
</style>