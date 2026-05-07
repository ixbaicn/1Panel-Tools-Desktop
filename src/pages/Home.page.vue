<script setup lang="ts">
import { onMounted } from 'vue';
import { useRouter } from 'vue-router';
import { useHead } from '@vueuse/head';
import { NSpin } from 'naive-ui';

const router = useRouter();

const title = '1Panel Tools Desktop';
const desc = 'Desktop wrapper for the Docker Compose to 1Panel AppStore tool';

useHead({
  title,
  meta: [
    {
      name: 'description',
      content: desc,
    },
    {
      property: 'og:title',
      content: title,
    },
    {
      property: 'og:description',
      content: desc,
    },
  ],
});

// 直接重定向到Docker Compose工具
onMounted(() => {
  router.replace('/docker-compose-to-1panel-appstore');
});
</script>

<template>
  <div class="flex items-center justify-center min-h-screen">
    <div class="text-center">
      <n-spin size="large" />
      <p class="mt-4 text-lg">正在跳转到 Docker Compose 转换工具...</p>
    </div>
  </div>
</template>

<style scoped>
</style>
