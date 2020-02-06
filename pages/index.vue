<template>
  <div>
    <NavBar/>
    <div class="hero">
      <img src="~assets/img/logo.png" alt="gikencraft"/>
      <b-button variant="outline-light" to="/about">Learn more</b-button>
    </div>
    <Container>
      <b-container>
        <b-row>
          <b-col sm="8">
            <p class="h3">新着情報</p>
            <b-table bordered striped :fields="informations_fields" :items="informations" :sort-by.sync="informations_sortBy"/>
          </b-col>
          <b-col sm="4">
            <p class="h3">メンバー</p>
            <b-table bordered striped :fields="members_fields" :items="members" :sort-by.sync="members_sortBy"/>
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

  export default {
    components: {
      Container,
      Footer,
      NavBar
    },
    data() {
      return {

      }
    },
    async asyncData({ $axios }){
      const mambers_res = await $axios.$get('https://api.gikencraft.net/members');
      const informations_res = await $axios.$get('https://api.gikencraft.net/informations');
      return {
        members: mambers_res,
        informations: informations_res,
        members_fields:[
          "name",
        ],
        informations_fields:[
          "date",
          "content",
        ],
        members_sortBy: "name",
        informations_sortBy: "date",
      }
    }
  }
</script>

<style scoped>
  .hero {
    margin: 0 auto;
    width: auto;
    height: 80vw;
    max-height: 600px;
    background: linear-gradient(45deg, rgba(46, 142, 35, 0.45), rgba(119, 106, 255, 0.45)), url("~assets/img/hero.jpg");
    background-size: cover;
    background-position: 50%;
    background-attachment: fixed;
    box-shadow: 0px 0px 8px 0px #222 inset;
    text-align: center;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .hero img {
    width: 80%;
    max-width: 500px;
    height: auto;
    margin-bottom: 32px;
    opacity: 0.9;
  }
</style>
