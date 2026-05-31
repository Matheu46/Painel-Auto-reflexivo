<script setup>
import { inject } from 'vue'
import SobreMimModern from './SobreMimModern.vue'
import SobreMimRetro from './SobreMimRetro.vue'

const isRetro = inject('isRetro')
</script>

<template>
  <component :is="isRetro ? SobreMimRetro : SobreMimModern" />
</template>
