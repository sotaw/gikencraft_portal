<template>
  <div class="container">
    <slot />
  </div>
</template>

<script>
  export default {
    name: "Container"
  }
</script>

<style scoped>
  .container{
    margin: 0 auto;
    max-width: 1000px;
    padding-top: 16px;
    padding-bottom: 16px;
  }
</style>
