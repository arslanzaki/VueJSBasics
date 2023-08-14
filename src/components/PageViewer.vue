<template>
  <div id="content" class="text-center">
    <h1 class="font-bold text-3xl">{{ page.pageTitle }}</h1>
    <p class="text-md makeBold">{{ page.pageContent }}</p>
  </div>
</template>

<script>
export default {
  props: ["page"],
};
</script>
