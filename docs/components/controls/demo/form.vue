<template>
  <n-pro-form :instance="form" :toolbars="toolbars" />
</template>

<script lang="ts" setup>
function delay(time: number) {
  return new Promise<void>(resolve => setTimeout(() => resolve(), time))
}

const form = defineForm({
  store: {
    type: 'input',
    placeholder: 'store id',
  },
  name: {
    type: 'input',
    placeholder: 'name',
  },
})

const toolbars = defineControls([
  {
    render: () => 'Search',
    helper: () => {
      return delay(1000)
    },
  },
  {
    type: 'default',
    render: () => 'Reset',
    helper: () => {
      return delay(1000)
    },
  },
])
</script>
