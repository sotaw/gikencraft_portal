<template>
  <b-navbar toggleable="lg" type="dark" variant="info">
    <b-navbar-brand to="/">
      <img class="main_logo" src="~assets/img/logo.png" alt="gikencraft"/>
    </b-navbar-brand>

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav>
        <b-nav-item to="/">Home</b-nav-item>
        <b-nav-item to="about">GikenCraftとは</b-nav-item>
        <b-nav-item to="/rules">ルール</b-nav-item>
        <b-nav-item-dropdown text="サーバ情報">
          <b-dropdown-item to="/detail">サーバ情報</b-dropdown-item>
          <b-dropdown-item to="/plugins">導入プラグイン</b-dropdown-item>
          <b-dropdown-item to="/permissions">パーミッション情報</b-dropdown-item>
          <b-dropdown-item to="/commands">コマンド一覧</b-dropdown-item>
          <b-dropdown-item href="http://gikencraft.net:8123" target="_blank">Dynmap</b-dropdown-item>
        </b-nav-item-dropdown>
      </b-navbar-nav>

      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto">
        <b-nav-item href="#">
          <img class="giken_logo" src="~assets/img/g_mark.png" alt="Kitten">
        </b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<script>
  export default {
    name: "NavBar"
  }
</script>

<style scoped>
  .main_logo {
    height: 36px;
  }

  .giken_logo {
    height: 28px;
  }
</style>
