<script setup lang="ts">
import { ref } from 'vue';
import CommonRadio from './components/CommonRadio/CommonRadio.vue'

const radioValue = ref('')
</script>

<template>
  <div>
    <section>
      <div>radio: {{ radioValue }}</div>
      <common-radio v-model="radioValue" :value="1" label="我是radio1"></common-radio>
      <common-radio v-model="radioValue" :value="2" label="我是radio2"></common-radio>
    </section>
  </div>
</template>

<style scoped>
</style>
