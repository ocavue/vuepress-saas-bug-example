<template>
    <div>
        vuepress-theme-project/Layout.vue is loaded
        <pre>{{ JSON.stringify(this.$site, null, "    ")}}</pre>
        <pre>{{ JSON.stringify(this.$page, null, "    ")}}</pre>
    </div>
</template>

<script>
export default {
  name: "app",
  data() {
    return {};
  }
};
</script>

<style>
</style>
