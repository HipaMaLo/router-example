<template>
 <h1>This a post {{ postId }} page</h1>

</template>

<script setup lang="ts">
import { onMounted, ref } from 'vue';
import { useRoute } from 'vue-router';

let postId = ref('');

onMounted(() => {
  const route = useRoute();
  postId.value = route.params.id.toString();
});

</script>