<template>
  <div class="globalTest">首页</div>
  <!-- 路由使用 -->
  <NuxtLink to="/home">home</NuxtLink>
  <NuxtLink to="/about">about</NuxtLink>
  <!-- 静态资源访问(public) -->
  <img
    class="imgSty"
    src="/01.jpg"
    alt=""
  />
  <!-- 静态资源访问(assets) -->
  <img
    src="@/assets/img/01.jpg"
    class="imgSty"
    alt=""
  />
  <!-- 编程式路由导航 -->
  <hr />
  <div>
    <!-- 无参数 -->
    <button @click="jumpNo">/about</button>
    <!-- 有参数 -->
    <button @click="jumpHas">/home</button>
  </div>
  <hr />
  <!-- 动态路由 -->
  <NuxtLink to="/details/1">/details</NuxtLink>
  <!-- 嵌套路由 -->
  <NuxtLink to="/parent/parent">/parent/parent</NuxtLink>
</template>
<script setup lang="ts">
const jumpNo = () => {
  navigateTo("/about", {
    replace: false,
    external: false,
  });
};

const jumpHas = () => {
  navigateTo({
    path: "/home",
    query: {
      type: "phone",
    },
    // params: {},
  });
};
</script>

<style scoped lang="scss">
.globalTest {
  color: $baseFontColor;
}

.imgSty {
  height: 100px;
}
</style>
