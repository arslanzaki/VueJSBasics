<template>
  <a
    class="text-white rounded-md px-3 py-2 text-sm font-medium"
    :class="{ 'makeBold': isActive }"
    aria-current="page"
    :key="index"
    :href="page.link.url"
    :title="`This link goes to ${page.link.text} Page`"
    >{{ page.link.text }}
  </a>
</template>

<script>
export default {
  props: ["page", "isActive"],
};
</script>

<style scoped>
    .makeBold {
        font-size: larger;
        font-weight: bolder;
    }
</style>
