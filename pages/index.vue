<template>
  <div>
    <NavBar/>
    <div class="hero">
      <img src="~assets/img/logo.png" alt="gikencraft"/>
      <b-button variant="outline-light">Learn more</b-button>
    </div>
    <b-container class="contents">
      <b-row>
        <b-col sm="8">
          <p class="h3">What's new</p>
          <b-table bordered striped hover :items="whatsnew"></b-table>
        </b-col>
        <b-col sm="4">
          <p class="h3">Members</p>
          <b-table bordered striped hover :items="members"></b-table>
        </b-col>
      </b-row>
    </b-container>
    <Footer/>
  </div>
</template>

<script>
  import NavBar from "~/components/NavBar";
  import Footer from "~/components/Footer";

  export default {
    components: {
      Footer,
      NavBar
    },
    data() {
      return {
        members: [
          {user: 'user1'},
          {user: 'user2'},
          {user: 'user3'},
          {user: 'user4'},
          {user: 'user5'},
          {user: 'user6'},
          {user: 'user7'},
          {user: 'user8'},
          {user: 'user9'}
        ],
        whatsnew: [
          {date: '2020.1.11', title: 'Now developing'},
          {date: '2020.1.11', title: 'Now developing'},
          {date: '2020.1.11', title: 'Now developing'},
          {date: '2020.1.11', title: 'Now developing'}
        ],
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

  .contents {
    margin: 0 auto;
    max-width: 1000px;
    padding-top: 32px;
  }
</style>
