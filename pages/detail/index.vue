<template>
  <div>
    <NavBar/>
    <Container>
      <Title>サーバ情報</Title>
      <b-container>
        <b-row>
          <b-col sm="6">
            <p class="h3">サーバ</p>
            <table class="table table-striped table-bordered">
              <tr>
                <td>ソフトウェア</td>
                <td>Spigot 1.15.1</td>
              </tr>
              <tr>
                <td>モード</td>
                <td>Survival</td>
              </tr>
              <tr>
                <td>難易度</td>
                <td>Easy</td>
              </tr>
              <tr>
                <td>シード値</td>
                <td>20180827</td>
              </tr>
              <tr>
                <td>スペック</td>
                <td>さくらVPS 2G (CPU:3cores, RAM:2GB)</td>
              </tr>
            </table>
          </b-col>
          <b-col sm="6">
            <p class="h3">接続情報</p>
            <table class="table table-striped table-bordered">
              <tr>
                <td>アドレス</td>
                <td>gikencraft.net</td>
              </tr>
              <tr>
                <td>ポート</td>
                <td>25565</td>
              </tr>
              <tr>
                <td>ホワイトリスト</td>
                <td>有効</td>
              </tr>
            </table>
          </b-col>
        </b-row>
      </b-container>
    </Container>
    <Footer/>
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
    }
  }
</script>

<style scoped>

</style>
