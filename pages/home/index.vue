<template>
  <div>home</div>
  <NuxtLink to="/">home</NuxtLink>
  <div>
    <ClientOnly>
      <!-- 
        在服务端渲染期间，fallback内容会被渲染,一般会显示加载信息
       -->
      <template #fallback>
        <p>该内容只会再服务器端渲染</p>
      </template>
    </ClientOnly>
    <ClientOnly>
      <template #default>
        <p>该内容会再客户端渲染</p>
      </template>
    </ClientOnly>
  </div>
</template>
<script setup lang="ts">
const route = useRoute();
console.log(route.query);
console.log(route.params);
</script>

<style scoped></style>
