<template>
  <div class="title">
    <span class="h1"><slot /></span>
  </div>
</template>

<script>
  export default {
    name: "Title"
  }
</script>

<style scoped>
  .title{
    margin-top: 32px;
    text-align: center;
    margin-bottom: 32px;
  }

  .title span{
    background: linear-gradient(transparent 60%, #F06292 0%);
    font-weight: 600;
  }

</style>
