<template>
  <Blog />
</template>

<script setup lang="ts">
import { provide } from 'vue';
import Blog from './Blog.vue';

export interface AuthorInterface {
  author: string;
  birthdate: number;
}

const author: AuthorInterface = {
  name: 'Chateaubriand',
  birthdate: 1768,
};

provide<AuthorInterface>('author', author);
</script>

<style scoped lang="scss"></style>
