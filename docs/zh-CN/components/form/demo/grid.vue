<template>
  <n-pro-form :instance="form" />
</template>

<script lang="ts" setup>
const form = defineForm({
  brandNum: {
    type: 'input',
    span: 12,
  },
  email: {
    type: 'input',
    span: 12,
  },
  time: { type: 'date-picker' },
})
</script>
