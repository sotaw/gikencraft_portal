<template>
  <div>
    <NavBar />
    <Container>
      <Title>導入プラグイン</Title>
      <b-table bordered striped :items="items" :sort-by.sync="sortBy">
        <template v-slot:cell(name)="data">
          <a v-bind:href="`${data.item.name.url}`" target="_blank">{{data.item.name.title}}</a>
        </template>
      </b-table>
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
        sortBy: "name.title",
        items: [
          {
            name: {title: "Dynmap", url: "https://www.spigotmc.org/resources/dynmap.274/"},
            version: "v3.0-beta-9-250",
            description: "ブラウザからサーバの地図を見られるようにする",
          },
          {
            name: {title: "TreeAssist", url: "https://www.spigotmc.org/resources/treeassist.67436/"},
            version: "v6.0.81",
            description: "木の伐採を支援する",
          },
          {
            name: {title: "NerfPhantoms", url: "https://www.spigotmc.org/resources/nerfphantoms.59218/"},
            version: "1.2.0",
            description: "ファントムの出現を無効化する",
          },
          {
            name: {title: "SetSpawn", url: "https://www.spigotmc.org/resources/setspawn-1-8-1-14-a-lot-of-features-fully-customisable.31966/"},
            version: "3.4",
            description: "初期スポーン地点へワープできるコマンドを追加する",
          },
          {
            name: {title: "LuckPerms", url: "https://www.spigotmc.org/resources/luckperms-an-advanced-permissions-plugin.28140/"},
            version: "5.0.39",
            description: "コマンドの実行権限を管理する",
          },
        ]
      }
    }
  }
</script>

<style scoped>

</style>
