<template>
  <div>details: id={{ id }}</div>
</template>
<script setup lang="ts">
const route = useRoute();
const id = route.params.id;
</script>

<style scoped></style>
