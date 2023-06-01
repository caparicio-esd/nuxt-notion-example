<template>
  <div class="menu w-[400px] bg-gray-100 p-4 sticky top-0 h-screen">
    <NuxtLink to="/">Al inicio</NuxtLink>
    <div class="menu_item" v-for="link in links">
      <NuxtLink :to="link.href">{{ link.title }}</NuxtLink>
    </div>
  </div>
</template>

<script setup>
const links = ref([
  { title: "Modern Tooling", href: "/esd/modern-tooling" },
  { title: "PostCss and Tailwind", href: "/esd/postcss" },
  { title: "Git y GitHub", href: "/esd/git" },
]);
</script>
