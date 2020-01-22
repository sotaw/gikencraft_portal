<template>
  <div>
    <NavBar />
    <Container>
      <Title>コマンド一覧</Title>
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
            command: "/list",
            description: "接続ユーザ一覧を表示",
            example: "/list"
          },
          {
            command: "/tell",
            description: "プライベートメッセージを送信",
            example: "/tell hojiro hogehoge"
          },
          {
            command: "/spawn",
            description: "初期スポーン地点へワープ",
            example: "/spawn"
          },
        ]
      }
    }
  }
</script>

<style scoped>

</style>
