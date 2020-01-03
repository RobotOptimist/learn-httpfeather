<template>
  <div class="bg-grey-100">
    <site-nav class="p-10 pb-0"></site-nav>
    <nuxt />
  </div>
</template>

<script>
import siteNav from '../components/siteNav';
export default {
  components: {
    siteNav
  }
}
</script>

<style>
  .h1 {
    @apply text-5xl text-green-600 font-semibold;
  }
</style>
