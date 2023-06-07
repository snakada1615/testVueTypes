<script setup lang="ts">
import { computed } from 'vue';
import { statusType } from '../types';
const props = defineProps({
  status: statusType().isRequired,
});
const value = computed(() => props.status || '-');
</script>
<template>
  <b>{{ value }}</b>
</template>
