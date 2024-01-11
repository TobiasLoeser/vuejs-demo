<script setup>
defineProps({
  listItem: {
    type: String,
    required: true
  }
})
</script>

<template>
  <li class="list-group-item list-group-item-primary"><i class="bi bi-arrow-right-square me-2"></i>{{ listItem }}</li>
</template>

<style scoped>

</style>
