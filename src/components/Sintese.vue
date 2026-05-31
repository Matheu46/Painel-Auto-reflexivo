<script setup>
import { inject } from 'vue'
import SinteseModern from './SinteseModern.vue'
import SinteseRetro from './SinteseRetro.vue'

const isRetro = inject('isRetro')
</script>

<template>
  <component :is="isRetro ? SinteseRetro : SinteseModern" />
</template>
