<template>
  <div>
    <NavBar />
    <Container>
      <Title>ルール</Title>
    </Container>
    <Footer />
  </div>
</template>

<script>
  import NavBar from "~/components/NavBar";
  import Footer from "~/components/Footer";
  import Container from "~/components/Container";
  import Title from "~/components/Title";

  export default {
    name: "index",
    components: {
      Title,
      Container,
      Footer,
      NavBar
    },
  }
</script>

<style scoped>

</style>
