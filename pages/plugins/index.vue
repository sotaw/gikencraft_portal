<template>
  <div>
    <NavBar />
    <Footer />
  </div>
</template>

<script>
  import NavBar from "~/components/NavBar";
  import Footer from "~/components/Footer";

  export default {
    name: "index",
    components: {
      Footer,
      NavBar
    },
  }
</script>

<style scoped>

</style>
