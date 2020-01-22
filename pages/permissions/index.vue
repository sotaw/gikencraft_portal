<template>
  <div>
    <NavBar />
    <Container>
      <Title>パーミッション情報</Title>
      <b-table bordered striped :items="items" />
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
    data() {
      return {
        items: [
          {
            permission: "minecraft.command.list",
            description: "/list コマンドの許可",
          },
          {
            permission: "minecraft.command.tell",
            description: "/tell コマンドの許可",
          },
          {
            permission: "dynmap.marker.sign",
            description: "看板を使用したマーカ作成の許可",
          },
          {
            permission: "spawn.spawn",
            description: "/spawn コマンドの許可"
          },
        ]
      }
    }
  }
</script>

<style scoped>

</style>
