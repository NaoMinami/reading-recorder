<template>
  <div id="app">
    <h2>Reading Recorder</h2>
    <div>
      <b-navbar toggleable="lg" type="dark" variant="info">
        <b-navbar-brand href="#">Menu</b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav>
            <b-nav-item>
              <router-link tag="b-nav-item" active-class="current" exact to="/"
                >Home</router-link
              >
            </b-nav-item>
            <b-nav-item>
              <router-link
                tag="b-nav-item"
                active-class="current"
                exact
                to="/search"
                >Search</router-link
              >
            </b-nav-item>
            <b-nav-item>
              <router-link
                tag="b-nav-item"
                active-class="current"
                exact
                to="/grid"
                >Grid</router-link
              >
            </b-nav-item>
          </b-navbar-nav>

          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto">
            <b-nav-form>
              <b-form-input
                size="sm"
                class="mr-sm-2"
                placeholder="Search"
              ></b-form-input>
              <b-button size="sm" class="my-2 my-sm-0" type="submit"
                >Search</b-button
              >
            </b-nav-form>

            <b-nav-item-dropdown text="Lang" right>
              <b-dropdown-item href="#">EN</b-dropdown-item>
              <b-dropdown-item href="#">ES</b-dropdown-item>
              <b-dropdown-item href="#">RU</b-dropdown-item>
              <b-dropdown-item href="#">FA</b-dropdown-item>
            </b-nav-item-dropdown>

            <b-nav-item-dropdown right>
              <!-- Using 'button-content' slot -->
              <template #button-content>
                <em>User</em>
              </template>
              <b-dropdown-item href="#">Profile</b-dropdown-item>
              <b-dropdown-item href="#">Sign Out</b-dropdown-item>
            </b-nav-item-dropdown>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </div>
    <!-- メインメニューを定義 -->
    <!--
    <el-menu
      mode="horizontal"
      background-color="#545c64"
      text-color="#fff"
      active-text-color="#ffd04b"
    >
      <el-menu-item index="1">
        <router-link to="/">Home</router-link>
      </el-menu-item>
      <el-menu-item index="2">
        <router-link to="/search">Search</router-link>
      </el-menu-item>
      -->
    <!-- サブメニューを定義 -->
    <!--
      <el-submenu index="3">
        <template v-slot:title>Support</template>
        <el-menu-item index="3-1">
          <a href="https://wings.msn.to/" target="help">Author</a>
        </el-menu-item>
        <el-menu-item index="3-2">
          <a href="https://www.sbcr.jp/" target="help">Publisher</a>
        </el-menu-item>
      </el-submenu>
    </el-menu>
    -->
    <router-view />
  </div>
</template>

<script>
export default {
  name: "app",
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.current {
  font-weight: bold;
}
</style>
