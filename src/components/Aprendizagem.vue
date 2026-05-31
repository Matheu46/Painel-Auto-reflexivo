<script setup>
import { inject } from 'vue'
import AprendizagemModern from './AprendizagemModern.vue'
import AprendizagemRetro from './AprendizagemRetro.vue'

const isRetro = inject('isRetro')
</script>

<template>
  <component :is="isRetro ? AprendizagemRetro : AprendizagemModern" />
</template>
