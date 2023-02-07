<script setup lang="ts">
import { reactive, ref } from 'vue';
import CommonRadio from './components/CommonRadio/CommonRadio.vue'
import CommonSelect from './components/CommonSelect.vue'

const radioValue = ref('')
</script>

<template>
  <div>
    <section>
      <div>radio: {{ radioValue }}</div>
      <common-radio v-model="radioValue" :value="1" label="我是radio1"></common-radio>
      <common-radio v-model="radioValue" :value="2" label="我是radio2"></common-radio>
    </section>
    <common-select>
      <li>1</li>
      <li>1</li>
      <li>1</li>
      <li>1</li>
    </common-select>
  </div>
</template>

<style scoped>
</style>
