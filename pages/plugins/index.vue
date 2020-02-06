<template>
  <div>
    <NavBar />
    <Container>
      <Title>導入プラグイン</Title>
      <b-table bordered striped :fields="fields" :items="items" :sort-by.sync="sortBy">
        <template v-slot:cell(name)="data">
          <a v-bind:href="`${data.item.url}`" target="_blank">{{data.item.name}}</a>
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

      }
    },
    async asyncData({ $axios }){
      const res = await $axios.$get('https://api.gikencraft.net/plugins');
      return {
        items: res,
        fields:[
          "name",
          "version",
          "description"
        ],
        sortBy: "name",
      }
    }
  }
</script>

<style scoped>

</style>
