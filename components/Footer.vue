<template>
  <div class="footer">
    <img src="~assets/img/logo.png" alt="gikencraft"/>
    <div class="copy">© 2020 Densigiken All Rights Reserved.</div>
  </div>
</template>

<script>
  export default {
    name: "Footer"
  }
</script>

<style scoped>
  .footer {
    margin: 0 auto;
    background: #222222;
    color: #FAFAFA;
    padding-top: 32px;
    padding-bottom: 32px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .footer img {
    max-width: 300px;
    width: 40%;
    opacity: 0.3;
    margin-bottom: 16px;
  }

  .copy{
    text-align: center;
    opacity: 0.5;
  }
</style>
