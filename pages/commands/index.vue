<template>
  <div>
    <NavBar />
    <Container>
      <Title>コマンド一覧</Title>
      <b-table bordered striped :fields="fields" :items="items" :sort-by.sync="sortBy" />
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

      }
    },
    async asyncData({ $axios }){
      const res = await $axios.$get('https://api.gikencraft.net/commands');
      return {
        items: res,
        fields:[
          "name",
          "description",
          "example",
        ],
        sortBy: "name",
      }
    }
  }
</script>

<style scoped>

</style>
